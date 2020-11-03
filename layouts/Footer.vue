<template>
  <div class="flex content-center flex-wrap bg-gray-200 h-32">
    <div class="flex-1 w-1/3 p-2 text-center">
      {{ title }} - {{ description }}
    </div>
    <div class="flex-1 w-1/3 p-2 text-center">{{ location }}</div>
    <div class="flex-1 w-1/3 p-2 text-center">
      <a :href="contact.github" target="_blank"
        ><GithubIcon
          class="p-2 icon transition duration-100 ease-in-out hover:text-teal-800 transform hover:-translate-y-1 hover:scale-110"
      /></a>
      <a :href="contact.linkedin" target="_blank"
        ><LinkedinIcon
          class="p-2 icon transition duration-100 ease-in-out hover:text-teal-800 transform hover:-translate-y-1 hover:scale-110"
      /></a>
      <a :href="contact.twitter" target="_blank"
        ><TwitterIcon
          class="p-2 icon transition duration-100 ease-in-out hover:text-teal-800 transform hover:-translate-y-1 hover:scale-110"
      /></a>
      <a :href="`mailto:{{contact.mail}}`" target="_blank"
        ><MailIcon
          class="p-2 icon transition duration-100 ease-in-out hover:text-teal-800 transform hover:-translate-y-1 hover:scale-110"
      /></a>
    </div>
  </div>
</template>
<script>
import GithubIcon from '../components/icons/GithubIcon.vue'
import LinkedinIcon from '../components/icons/LinkedinIcon.vue'
import TwitterIcon from '../components/icons/TwitterIcon.vue'
import MailIcon from '../components/icons/MailIcon.vue'

export default {
  name: 'Footer',
  components: {
    GithubIcon,
    LinkedinIcon,
    TwitterIcon,
    MailIcon,
  },
  data: () => {
    return {
      title: 'Alexis Barba',
      description: 'Web Developer',
      location: 'Tepic, Nayarit',
      contact: {
        github: 'https://github.com/alexbarba/',
        linkedin: 'https://www.linkedin.com/in/alexisbarba',
        twitter: 'https://www.twitter.com/alexbarba_',
        mail: 'alexis.barba.perez@gmail.com',
      },
    }
  },
}
</script>
