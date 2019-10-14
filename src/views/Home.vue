<template>
  <div class="resume-container" :class="{'egg': spin}" >
    <i class="spin" @dblclick="spin = !spin"></i>
    <header>
      <h2>JuanRodriguez</h2>
      <h6>A Front-End Developer with an expertise in modern HTML - CSS - JavaScript across various frameworks, extensive insight on user interaction, web
      layouts, and responsive design.
      </h6>
    </header>
    <main>
      <experience-section :experience="experience"/>
      <education-section :education="education"/>
      <community-section :community="community"/>
      <skills-section :skills="skills"/>
    </main>
    <footer>
      <p>Austin, Texas</p>
      <p>juan.j.rodriguez2@gmail.com</p>
      <p>956.454.7611</p>
      <p>juanrod.co</p>
      <p>github.com/juan-rod</p>
      <p>linkedin.com/in/juanrod1</p>
    </footer>
  </div>
</template>

<script>
// @ is an alias to /src
import ExperienceSection from '@/components/ExperienceSection.vue'
import EducationSection from '@/components/EducationSection.vue'
import CommunitySection from '@/components/CommunitySection.vue'
import SkillsSection from '@/components/SkillsSection.vue'

export default {
  name: 'home',
  components: {
    ExperienceSection,
    CommunitySection,
    SkillsSection,
    EducationSection,
  },
  mounted () {
    setTimeout(() => {
      // this.show = true
    }, 1000);
  },
  data () {
    return {
      spin: false,
      show: false,
      experience: [
        {
          date: 'March 17 - August 18',
          company: 'MediaScience Labs',
          position: 'Front End Developer',
          workList: [
            'Manage Media Science’s user facing projects',
            'Maintain panelist site by updating and pushing improvements on a daily basis',
            'Created a central panelist dashboard that allows users to: submit surveys, update profile information, enter into a points/rewards system',
            'Created a texting module for direct access to users using twilio api',
            'Partner with marketing team to implement online campaign initiatives',
            'Troubleshoot potential programming issues at on-site studies'
          ]
        },
        {
          date: 'March 16 - Sept 17',
          company: 'DCR Point-of-Sales Systems',
          position: 'Associate Developer',
          workList: [
            'Implemented user friendly features for the in-house data monitoring system',
            'Created a department specific website to showcase new projects',
            'Refactored existing code to reduce the risk of error',
            'Installed OTA updates to stores around the country'
          ]
        }
      ],
      education: [
        {
          date: 'July 15 - Dec 15',
          school: 'Nashville Software School',
          subtitle: 'Web Developer',
          workList: [
            'A six-month, full-time software boot camp for problem-solving web development',
            'Created individual and collaborative single page applications',
            'Implemented MVC design patterns',
            'Utilized Git in a team environment'
          ]
        },
        {
          date: 'August 06 - Dec 10',
          school: 'Texas State University',
          subtitle: 'B.A. in Theatre'
        },
      ],
      community: [
        {
          date: 'March 17 - August 19',
          position: 'Technology Director',
          org: 'The Austin Gay and Lesbian Pride Foundation'
        }
      ],
      skills: [
        'HTML',
        'CSS',
        'Javascript',
        'SASS',
        'ES6',
        'Vue.js',
        'Firebase',
        'Git',
        'Webpack',
        'Sketch',
      
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.fadeOne-enter-active, .fadeOne-leave-active {
  transition: all .5s ease-out;
}
.fadeOne-enter, .fadeOne-leave-to {
  clip-path: polygon(0% 0%, 100% 0%, 100% 0%, 0% 0%);
  transform: translate(0%, 100%);
}
// .fadeOne {
//     &-enter-active,
//     &-leave-active {
//       transition: all .5s ease-out;
//     }
//     &-enter,
//     &-leave-to {
//       clip-path: polygon(0% 0%, 100% 0%, 100% 0%, 0% 0%);
//       transform: translate(0%, 100%);
//     }
//   }
</style>
