<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script>
import {mapGetters} from 'vuex';

export default {
  name:'About',
  computed:{
    ...mapGetters({
      ticket:'ticket'
    })
  },
  methods:{
    goToHome(){
      this.$router.push('/')
    }
  }
}
</script>

<style>
  .about{
    display: flex;
    justify-content: center;
    align-items: center;
    height:100% ;
  }
  .form{
    width: 450px;
    height: 300px;
    background-color:red;
    box-shadow: 1px 1px 25px 2px cornsilk;
    text-align: center;
    align-content: center;
  }
  .title{
    margin-top: 50px;
  }
  .button{
    margin-top: 80px;
  }
  button{
    outline: none;
    cursor: pointer;
    border: 1px solid black;
    border-radius: 5px;
    padding:10px 40px;
  }      
  .link{
    margin-top:50px;
    margin-right:10px;
    text-align: right;
    text-decoration: underline;
    cursor: pointer;
  }

</style>

