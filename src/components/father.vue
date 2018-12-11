<template>
<div>
    <button @click="clickParent">{{yuandou}}</button>
    <son ref="mychild" :shuxing = "yuandou" @event="getuser"></son>
  </div>
</template>

<script>
 import son from './son';
export default {
    data() {
      return {
            // radio:'',
            c_zfb: true,
            c_wx: false,
            money: 'true',
            orderlist: [],
            rmb: '10',
            yuandou: '1000',
            access_code: '',
            userid: '',
            appVersion:'',
            isDisable: false,
            yuandouyue:'',
            channelList:'',
            zfbpay:'',
            wxpay:''
        }
    },
    name: "parent",
    components: {
      son:son
    },
    methods: {
      clickParent(e) {
        this.$refs.mychild.parentHandleclick(e);
      },
      getuser(e){
        console.log(e)
      }
    }
}
</script>

<style>

</style>
