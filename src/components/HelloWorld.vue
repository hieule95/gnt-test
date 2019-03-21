<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Lê Hoàng Minh Hiếu</h2>
    <h3>hieulhminh@gmail.com</h3>
    <div class="button-wrapper">
      <div class="button-wrapper-inner">
        <div class="button-item">
          <button class="btn btn-clickable" v-on:click="_redirectPage()"><span
              class="btn--text">{{ buttonMsg }}</span></button>
        </div>
        <div class="button-item">
          <button disabled class="btn btn-disabled"><span class="btn--text">{{ buttonMsg }}</span></button>
        </div>
        <div class="button-item">
          <button class="btn btn-clickable" v-on:click="_redirectPage()"><span
              class="btn--text">{{ buttonMsg }}</span></button>
        </div>
        <div class="button-item">
          <button disabled class="btn btn-disabled"><span class="btn--text">{{ buttonMsg }}</span></button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Welcome to my test',
        buttonMsg: 'Coming Soon'
      }
    },
    methods: {
      _redirectPage() {
        window.location.href = "https://google.com";
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Domine:400,700&subset=latin-ext');

  h1,
  h3 {
    font-weight: normal;
  }

  .button-wrapper {
    margin: auto;
  }

  .button-wrapper-inner {
    padding: 7rem;
    width: 300px;
    margin: auto;
    background: #82817f;
  }

  .button-item {
    width: 285px;
    margin: auto;
    overflow: hidden;
    margin-bottom: 2.5rem;
  }

  .btn {
    width: 100%;
    height: 80px;
    font-size: 1.8rem;
    font-weight: 700;
    color: white;
    border: none;
  }

  .btn-clickable {
    cursor: pointer;
    background: url('../assets/button_bg-1.png') no-repeat center;
    /* box-shadow: inset 0px 0px 0px 8px rgba(237,132,131,1); */
  }

  .btn-disabled {
    background: url('../assets/button_disable.png') no-repeat center;
    /* box-shadow: inset 0px 0px 0px 8px rgba(237,132,131,1); */
    cursor: not-allowed;
  }

  .btn--text {
  font-family: Domine, Helvetica Light, sans-serif;
  font-size: 1.4rem;
  font-weight: 700;
  text-align: center;
  letter-spacing: 5px;
  background: -webkit-linear-gradient( -90deg,    #5f5476 15%,    #b7a6db 25%,  #5f5476 45%, #b7a6db 75%, #444444 80%  );
  -webkit-background-clip: text;
  -webkit-text-stroke: 10px transparent;
  color: rgb(255, 255, 255);
  }
</style>