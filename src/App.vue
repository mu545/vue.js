<template>
  <div id="app">
    <header id="header">
      <nav>
        <router-link :to="{ path: '/' }">
            <img src="@/assets/logo.png">
            <span>Components</span>
        </router-link>
      </nav>
    </header>

    <section id="container">
      <router-view></router-view>
    </section>

    <footer id="footer">
      <p>
        <span>Copyright &copy; 2019 </span>
        <a href="https://github.com/mu545" target="__blank">Musa Sutisna</a></p>
    </footer>
  </div>
</template>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-size: 15px;
}

body {
  background: #F0F0F0;
}

#app {
  position: fixed;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
}

#header {
  width: 100%;
  min-height: 50px;
  background: #FFFFFF;
  box-shadow: 0 0 1em #999999;
}
#header nav {
  display: flex;
  width: 100%;
  margin: 10px;
  justify-content: center;
}
#header a {
  display: flex;
  align-items: center;
  text-decoration: none;
}
#header a img {
  width: 48px;
  height: 48px;
}

#container {
  display: flex;
  flex-grow: 1;
}

#footer {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
#footer p {
  margin: 10px;
  text-align: center;
}
</style>
