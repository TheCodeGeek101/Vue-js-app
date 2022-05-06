<script>

import HelloWorld from './components/HelloWorld.vue'
import Greet from './components/Greet.vue'
import TheWelcome from './components/TheWelcome.vue'
import Article from './components/Article.vue'
import TabA from './components/TabA.vue'
import TabB from './components/TabB.vue'
import TabC from './components/TabC.vue'
import Portal from './components/portal.vue'
import PostList from './components/PostList.vue'
import CreatePosts from './components/CreatePosts.vue'

export default {
  name: "App",
  components: {
    Greet,
    Article,
    TabA,
    TabB,
    Portal,
    PostList,
    TabC,
    CreatePosts,
    Parent,
  },
data(){
  return {
    name: "Thembinkosi",
    channel: "My channel",
    activeTab: "TabA",
  }
}
}

</script>

<template>

<CreatePosts />
<PostList />
<Parent />

</template>

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
