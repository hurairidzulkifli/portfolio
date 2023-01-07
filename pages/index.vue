<template>
  <b-row style="margin-left: 0; margin-right: 0">
    <b-col md="4">
      <b-img
        src="https://avatars.githubusercontent.com/u/38495309?s=96&v=4"
        id="avatar-img"
        alt=""
      />
    </b-col>

    <b-col md="8">
      <h2 class="intro animate__animated animate__fadeInUp animate__fast">
        Hi!,
        <br />I<span>'m Hurairi Dzulkifli</span>.
      </h2>

      <div class="col-md-10 info">
        A <b> Backend Developer </b> who specializes in the development of server-side web applications using the <b> Laravel </b> web application framework and a bit of <b>Vue</b> .
        <br />
        I solemnly swear i am fun to work with 😁.
        <br />
        <b-button
          class="action-btn animate__animated animate__wobble animate__delay-4s animate__fast"
          to="/about"
        >
          Explore >
        </b-button>

        <b-button
          class="action-btn"
          href="https://www.linkedin.com/in/hurairi-dzulkifli/"
          variant="primary"
          target="_blank"
        >
          Get In Touch
        </b-button>

        <!-- .SOCIAL LINKS SECTION -->
        <div
          class="social-icons animate__animated animate__fadeInUp animate__delay-1s"
        >
          <social-link :to="socialLinks.github">
            <GithubIcon />
          </social-link>

          <social-link :to="socialLinks.linkedin">
            <LinkedinIcon />
          </social-link>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
import GithubIcon from "vue-ionicons/dist/logo-github.vue";
import LinkedinIcon from "vue-ionicons/dist/logo-linkedin.vue";
import TwitterIcon from "vue-ionicons/dist/logo-twitter.vue";
import FacebookIcon from "vue-ionicons/dist/logo-facebook.vue";
import YoutubeIcon from "vue-ionicons/dist/logo-youtube.vue";
import MailIcon from "vue-ionicons/dist/md-mail.vue";

export default {
  components: {
    GithubIcon,
    LinkedinIcon,
    TwitterIcon,
    FacebookIcon,
    YoutubeIcon,
    MailIcon,
  },

  data() {
    return {
      avatar: require("@/assets/avatar-1.webp"),
      // ADD YOUR SOCIAL LINKS HERE 👇
      socialLinks: {
        github: "https://github.com/hurairidzulkifli",
        linkedin: "https://www.linkedin.com/in/hurairi-dzulkifli/",
      },
    };
  },

  head: {
    title: "HD Dashbord",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "A Lightweight and Stable Discord Music Bot For Your Daily Production.",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "HD Dashbord",
      },
      {
        property: "og:description",
        content:
          "A Lightweight and Stable Discord Music Bot For Your Daily Production.",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: "https://i.imgur.com/UmWcMjO.png",
      },
    ],
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();

      setTimeout(() => this.$nuxt.$loading.finish(), 500);
    });
  },
};
</script>
