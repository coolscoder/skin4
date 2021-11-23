<template>
  <link rel="stylesheet" 
    href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" 
    integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" 
    crossorigin="anonymous"
  >
  <div container>
    <div title v-text="title" />
    <div data-link-container>
      <div
        data-link
        v-for="(link, index) in links"
        v-bind:key="index"
      >
        <div v-text="link" />
        <i class="fas fa-location-arrow"></i>
      </div>
    </div>
    <div description v-text="description" />
  </div>
</template>

<script>
  export default {
    name: 'App',
    data: () => ({
      title: "FATIMA",
      links: [
        'YOUTUBE',
        'SPOTIFY',
        'DISCORD',
        'TIKTOK',
      ],
      description: "This is the best description in the freaking world its so great"
    }),
  }
</script>

<style>
  body {
    background: #fff;
    color: #fff;
    font-family: Helvetica;
    font-weight: bold;
    margin: 0;
  }
  [container] {
    background-color: #fff;
    border-radius: 20px;
    padding: 3vh;
    min-height: 94vh;
    overflow: hidden;
    background-color: #00bdd4;
  }
  [title] {
    text-align: center;
    font-size: 80px;
    height: 45vh;
    color: #fed521;
  }
  [data-link-container] {
    display: flex;
    flex-direction: column;
    height: 40vh;
    justify-content: space-around;
  }
  [data-link] {
    padding: 15px;
    background: black;
    display: flex;
    justify-content: space-between;
  }
  [description] {
    margin-top: 10px;
    text-align: center;
    color: black;
  }
</style>
