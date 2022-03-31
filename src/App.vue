<template>
  <div id="app">
      <header>
        <div class="size">
          <a href="/" class="logo">КУРТ КОБЕЙН</a>
        </div>
      </header>
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Underdog&display=swap");

body {
  padding: 0;
  margin: 0;
  background: black;
}

#app {
  font-family: "Underdog", cursive;
}

.size {
  width: 1440px;
  margin: 0 auto;
}

header {
  height: 200px;
  background: black;

  .size {
    display: flex;
    justify-content: space-between;
    text-align: center;

    .logo {
      margin-top: 20px;
      font-weight: bold;
      font-size: 144px;
      line-height: 166px;
      text-decoration: none;
      color: #f6d891;
      margin-left: 245px;
    }
  }
}
</style>
