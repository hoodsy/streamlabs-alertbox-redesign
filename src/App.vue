<template>
  <div id="app">
    <nav class="dashboard-nav nav">
      <span>nav</span>
    </nav>
    <section class="dashboard-content">
      <aside class="dashboard-sidenav nav">
        <span>sidenav</span>
      </aside>
      <div class="dashboard-body">
        <div class="section-header">
          <h3 class="section-heading">Alert Box</h3>
          <p class="section-text">Engage your audience with on-stream notification popups.</p>
        </div>
        <AlertBoxThemeSlider />
      </div>
    </section>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import AlertBoxThemeSlider from "./components/AlertBoxThemeSlider.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    AlertBoxThemeSlider
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");

html,
body,
#app {
  margin: 0;
  min-height: 100vh;
}

#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #1a242c;
  color: #ffffff;
}

.nav {
  display: flex;
  align-items: center;
  justify-content: center;
}

.dashboard-nav {
  height: 90px;
  margin-bottom: 32px;
  border-bottom: 1px solid #2a383f;
}

.dashboard-content {
  display: flex;
}

.dashboard-sidenav,
.dashboard-body {
  margin-right: 32px;
}

.dashboard-sidenav {
  min-width: 240px;
}

.dashboard-body {
  width: 100%;
  max-width: 1600px;
}

.section-header {
  margin-bottom: 24px;
}

.section-heading {
  font-size: 20px;
  margin: 0;
}

.section-text {
  color: #bdc2c4;
  font-size: 14px;
  margin-top: 4px;
  margin-bottom: 4px;
}
</style>
