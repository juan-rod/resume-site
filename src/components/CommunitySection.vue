<template>
<div class="community">
  <div class="section-title"> Community </div>
  <section v-for="(ex, index) in community" :key="index">
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
          <div class="detail-title">{{ ex.position }}</div>
          <div class="detail-subtitle">{{ ex.org }}</div>
          <div class="detail-body">
            <ul>
              <li v-for="(listItem, index) in ex.workList" :key="index"> {{listItem}} </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'CommunitySection',
  props: {
    community: Array
  }
}
</script>