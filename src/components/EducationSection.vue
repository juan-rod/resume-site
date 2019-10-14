<template>
<div>
  <div class="section-title"> Education </div>
  <section v-for="(ex, index) in education" :key="index">
      <div class="section-body">
        <div class="date">
          <p>{{ ex.date }}</p>
        </div>
        <div class="timeline education">
          <div class="timeline-circle circle-outer">
            <div class="inner"></div>
          </div>
          <div class="timeline-line"></div>
        </div>
        <div class="detail">
          <div class="detail-title">{{ ex.school }}</div>
          <div class="detail-subtitle">{{ ex.subtitle }}</div>
          <div class="detail-body">
            <ul>
              <li v-for="(listItem, index) in ex.workList" :key="index">
                <i class="fa fa-dot-circle-o" aria-hidden="true"></i>
                <p> {{listItem}} </p>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'EducationSection',
  props: {
    education: Array
  }
}
</script>