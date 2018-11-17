<!-- <template lang="html">
  <div class="aaa">
    <div class="bbb">
    ハロー, I'm hoola!!
    <div class="ccc">
    趣味は{{syumi}}
    <div class="ddd">
      走行距離は{{kyori}}km
        <button
    type="button"
    name="button"
    @click="plus">距離を足す
  </button>
    </div>
  </div>
  {{reverse}}
      <div :class="['hide', seven]">
      click 307 times
    </div>
    {{title.id}}
    {{title.name}}
  </div>
  </div>
</template> -->
​<template lang="html">
  <div class="sample">
    <div>
      <slot/>

    </div>
    <div class="blue">
      <h2>サンプルコンポネント</h2>
      <slot name="named"/>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      name:'hori',
      syumi:'自転車',
      kyori:300,
    }
  },
  methods: {
    plus(){
      this.kyori++
    }
  },
  computed:{
    reverse(){
      return this.name+"です"
    },
    seven(){
      return this.kyori === 307 ? 'seven':null;
    }
  },
  mounted(){
    console.log('hahaha')
  },
  props: ['title'],
}
</script>
​
<style lang="scss" scoped>
.ccc{
  color: blue;
}
.seven{
  color:yellow;
}
</style>