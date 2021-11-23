<template>
  <div container>
    <div title v-text="title" />
    <div data-link-container>
      <div
        data-link
        v-for="(link, index) in links"
        v-bind:key="index"
        v-text="link"
      />
    </div>
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

<style lang="scss">
  body {
    background: #fff;
    color: #fff;
    font-family: Helvetica;
    font-weight: bold;
    text-align: center;
    margin: 0;
  }
  [container] {
    background-color: #fff;
    border-radius: 20px;
    padding: 3vh;
    height: 94vh;
    overflow: hidden;
    background-color: black;
  }
  [title] {
    font-size: 60px;
    height: 30vh;
    color: #d1ac6b;
    display: flex;
    align-items: center;
  }
  [data-link-container] {
    display: flex;
    flex-direction: column;
    height: 64vh;
    justify-content: space-around;
  }
  [data-link] {
    width: 100%;
    padding: 15px 0;
    border: 1px solid white;
    background: transparent;
    &:hover {
      color: #cb1f63;
      background-color: #ede3b9;
    }
  }
</style>
