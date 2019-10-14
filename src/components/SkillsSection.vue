<template>
<div class="skills">
  <div class="section-title"> Skills </div>
  <section>
      <div class="section-body">
        <div class="date"></div>
        <div class="timeline">
          <div class="timeline-circle circle-outer">
            <div class="inner"></div>
          </div>
          <!-- <div class="timeline-line"></div> -->
        </div>
        <div class="detail">
          <div class="detail-body">
            <ul>
              <li v-for="(skill, index) in skills" :key="index"> {{skill}} </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'SkillsSection',
  props: {
    skills: Array
  }
}
</script>