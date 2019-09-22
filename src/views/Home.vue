<template>
  <div class="content">
    <div
      class="component-item"
      v-for="(component, key) in components"
      :key="key">
      <div class="title">
        <span class="name">{{ component.name }}</span>
        <span class="version">{{ component.version }}</span>
      </div>
      <div class="description">{{ component.description }}</div>
      <div class="link">
        <router-link :to="{ path: '/component/' + component.name.replace(/ /g, '-') }">
          open
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data: function () {
    return {
      components: this.$store.state.components
    }
  }
}
</script>

<style>
#container .content {
  display: flex;
  width: 100%;
  flex-direction: column;
}
#container .content .component-item {
  margin: 50px;
  padding: 30px;
  background: #FFFFFF;
}
#container .content .component-item .title {
  display: flex;
  align-items: flex-end;
}
#container .content .component-item .title .name {
  flex-grow: 1;
  font-size: 2em;
  text-align: left;
  text-transform: capitalize;
}
#container .content .component-item .title .version {
  flex-grow: 2;
  text-align: right;
}
#container .content .component-item .description {
  padding: 1em;
  margin: 0.5em 0;
  background: #F9F9F9;
}
#container .content .component-item .link {
  display: flex;
  margin: 0.5em 0;
  justify-content: flex-end;
}
#container .content .component-item .link a {
  padding: 0.5em;
  color: #FFFFFF;
  text-decoration: none;
  background: #666666;
}
</style>
