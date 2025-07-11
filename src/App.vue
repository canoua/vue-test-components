<template>
  <div>
    <User @my-event="handleMyEvent" @btn1-event="handleBtn1" @btn2-event="handleBtn2" />
    <p>{{ messageFromChild }}</p>
    <p>{{ messageFromBtn1 }}</p>
    <p>{{ messageFromBtn2 }}</p>
    <ParamsEvent  @show="func('Andrew', 'Kar')"/>

  </div>
</template>

<script>
  import User from './components/User.vue';
  import ParamsEvent from './components/ParamsEvent.vue';
  
  export default {  
    components: {
      User,
      ParamsEvent
    },
    data() {
      return {
        messageFromChild: '',
        messageFromBtn1: '',
        messageFromBtn2: ''
      }
    },
    methods: {
      handleMyEvent(data) {
        this.messageFromChild = data.message;
      },
      handleBtn1(data) {
        this.messageFromBtn1 = data.message
      },
      handleBtn2(data) {
        this.messageFromBtn2 = data.message
      },
      func(arg1, arg2) {
        console.log(arg1, arg2);
      }
    }
  }
</script>