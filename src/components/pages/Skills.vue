<template>
  <div class="skills">
    <page-content :heading="$route.name" :description="description"/>
    <div class="skill-list">
      <skill v-for="skill in skills" :heading="skill.heading" :list="skill.list" :key="skill.id"/>
    </div>
  </div>
</template>

<script>
import PageContent from '@/components/blocks/PageContent'
import Skill from '@/components/blocks/Skill'

export default {
  name: 'skills',
  components: {
    'page-content': PageContent,
    'skill': Skill
  },
  data () {
    return {
      description: `
        <p>While my last decade of work has primarily focused on Wordpress and Laravel,<br class="d-none d-md-block"> I've shifted my area of focus to Vue and React for the last 2 years.</p>
        <p>As a kid, my dream job was to work for a sweet video game dev like Nintendo or Sega.<br class="d-none d-md-block"> While I haven't achieved that goal yet, I've used this passion for video games to help<br class="d-none d-md-block"> sharpen my coding skills and create the games of my dreams using Unity 3D.</p>
      `,
      skills: [
        {
          heading: 'Web',
          list: ['HTML5', 'JS', 'CSS3/SCSS', 'PHP', 'Responsive Design', 'Canvas/WebGL']
        },
        {
          heading: 'JS: Vue',
          list: ['Vue.js', 'Nuxt.js', 'Vuex', 'Bootstrap Vue']
        },
        {
          heading: 'JS: React',
          list: ['React', 'Redux', 'Styled Components', 'React Bootstrap']
        },
        {
          heading: 'JS: Misc',
          list: ['Axios', 'Electron', 'Express', 'ES6', 'Node', 'Webpack', 'Jest', 'jQuery']
        },
        {
          heading: 'PHP',
          list: ['Laravel', 'Wordpress', 'Magento', 'Joomla', 'Drupal']
        },
        {
          heading: 'Wordpress',
          list: ['Sage', 'Bedrock', 'Trellis', 'ACF Pro', 'Gutenberg', 'WPEngine', 'Kinsta']
        },
        {
          heading: 'Unity 3D',
          list: ['C#', 'UI', 'Dialogue System', 'MasterAudio', 'Playmaker', 'Bolt', 'DOTween Pro']
        },
        {
          heading: 'Database & Query',
          list: ['MySQL', 'Postgres', 'SQLite', 'MariaDB', 'Firebase', 'GraphQL', 'Elasticsearch']
        },
        {
          heading: 'CLI',
          list: ['Git', 'NPM/Yarn', 'WP-CLI', 'Brew', 'Grunt', 'Bower']
        },
        {
          heading: 'Tools: Coding',
          list: ['VS Code', 'Transmit', 'iTerm', 'Sequel Pro']
        },
        {
          heading: 'Tools: Design ',
          list: ['Sketch', 'Photoshop', 'Illustrator', 'After Effects', 'Final Cut Pro']
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
