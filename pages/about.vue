<template>
  <section class="container">
    <div>
      <h1 class="title">
        nuxttest2
      </h1>
      <h2 class="subtitle">
      	<div class="aaa">
      		<div class="bbb">ペッポオー</div>
      		<div class="ccc">ひゃっこ</div>
          <nuxt-link to="/">topへ</nuxt-link>

    </div>
      </h2>
      <sample-component :title=pppp></sample-component>
    </div>
  </section>
</template>

<script>
import SampleComponent from '~/components/SampleComponent.vue'
export default {
  head () {
    return {
      // タイトルテンプレートがある場合は "ABOUT - ポートフォリオ" になる
      title: 'ABOUT',
      meta: [
        { hid: 'description', 
        name: 'description', 
        content: 'About ページをnuxtで作成をしております' }
      ]
    }
  },
  components: {
    SampleComponent
  },
  data(){
    return{
      pp:'hori',
      ppp:'自転車',
      pppp:{
      	id:900,
      	name:'吉田'
      }
    }
  },
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
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
