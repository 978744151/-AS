<template>
    <div>son</div>
</template>

<script>
export default {
    data(){
        return {
            obj:{
                num:'12',
                sas:'123'
            }
        }
    },
    name: "son",
    props: ['shuxing'],
    methods: {
      parentHandleclick(e) {
        console.log(this.shuxing)
        this.$emit('event',this.obj)
      }
    }
  }
</script>

<style>

</style>
