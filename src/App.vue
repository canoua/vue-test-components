<template>
  <div>
    <User @my-event="handleMyEvent" @btn1-event="handleBtn1" @btn2-event="handleBtn2" />
    <p>{{ messageFromChild }}</p>
    <p>{{ messageFromBtn1 }}</p>
    <p>{{ messageFromBtn2 }}</p>
    <ParamsEvent  @show="func('Andrew', 'Kar')"/>
    <AttrEvent @show="attrAlert"/>
  </div>
</template>

<script>
  import User from './components/User.vue';
  import ParamsEvent from './components/ParamsEvent.vue';
  import AttrEvent from './components/AttrEvent.vue';
  
  export default {  
    components: {
      User,
      ParamsEvent,
      AttrEvent
    },
    data() {
      return {
        messageFromChild: '',
        messageFromBtn1: '',
        messageFromBtn2: '',
        attr1: '',
        attr2: ''
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
      },
      attrAlert(attr1, attr2) {
        this.attr1 = attr1
        this.attr2 = attr2
      }
    }
  }
</script>