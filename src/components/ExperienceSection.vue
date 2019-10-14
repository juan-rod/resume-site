<template>
<div>
  <div class="section-title"> Experience </div>
  <section v-for="(ex, index) in experience" :key="index">
      <div class="section-body">
        <div class="date">
          <p>{{ ex.date }}</p>
        </div>
        <div class="timeline">
          <div class="timeline-circle circle-outer">
            <div class="inner"></div>
          </div>
          <div class="timeline-line"></div>
        </div>
        <div class="detail">
          <div class="detail-title">{{ ex.company }}</div>
          <div class="detail-subtitle">{{ ex.position }}</div>
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
  name: 'ExperienceSection',
  props: {
    experience: Array
  }
}
</script>

