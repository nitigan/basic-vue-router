<template>
  <div class="about">
    <div class="form">
      <div class="title">
        <h1> Ticket Remind </h1>
      </div>
      <div class="ticket">
        <h1>{{ticket}} tickets</h1>
      </div>
      <div class="link" @click="goToHome"> back </div>
    </div>
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
  .home{
    display: flex;
    justify-content: center;
    align-items: center;
    height:100% ;
  }
  .form{
    width: 450px;
    height: 300px;
    background-color: aliceblue;
    box-shadow: 1px 1px 25px 2px cornsilk;
    text-align: center;
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

