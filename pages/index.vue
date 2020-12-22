<template>
  <div></div>
  <!-- <div class="container">
    <div>
      <Logo />
      <h1 class="title">kcloud-powerapps-code</h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div> -->
</template>

<script>
export default {
  mounted(){
    this.movePowerApps();
  },
  methods:{
    movePowerApps() {
      const param = this.$route.query
      console.log(param)
        let url = 'https://apps.powerapps.com/play/fc13877c-4a28-4dc8-8d85-fbccc7861339?tenantId=65e49381-bb52-4f23-b50f-9fcab2c7e7db'
      // if (!param["hidenavBar"]) {
      //   url = url + '&hidenavBar=true'
      //   delete param["hidenavBar"]
      // }

      const url_get = jQuery.param( param );
      if (url_get != "") {
        url = url + '&' + url_get
      }
      window.location.href = url;
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
