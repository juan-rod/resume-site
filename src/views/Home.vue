<template>
  <div class="resume-container border1">
    <header>
      <h2>JuanRodriguez</h2>
      <h6>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi fugit voluptatum hic nesciunt soluta harum, sed assumenda aspernatur consectetur ipsa cupiditate impedit facere libero quo nemo explicabo dolor repudiandae temporibus.</h6>
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
  data () {
    return {
      experience: [
        {
          date: 'March 2017 - August 2018',
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
          date: 'March 2016 - Sept 2017',
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
          date: 'July 2015 - Dec 2015',
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
          date: 'August 2006 - Dec 2010',
          school: 'Texas State University',
          subtitle: 'B.A. in Theatre'
        },
      ],
      community: [
        {
          date: 'March 2017 - August 2019',
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
