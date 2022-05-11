<script>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import PostList from './components/PostList.vue'
import CreatePosts from './components/CreatePosts.vue'
import TemplateRef from './components/TemplateRef.vue'
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'
import Data from './components/Data.vue'
import DemoOne from './components/DemoOne.vue'
import DemoTwo from './components/DemoTwo.vue'
import Methods from './components/Methods.vue'
import VModel from './components/VModel.vue'
import Computed from './components/Computed.vue'
import Watch from './components/Watch.vue'
import Provideinject from './components/Provideinject.vue'
import TempRef from './components/TempRef.vue'
import Person from './components/Person.vue'
import PersonGreeting from './components/PersonGreeting.vue'

export default{
  name:"App",
  components:{
    PersonGreeting,
    Person,
    TempRef,
    Watch,
    Provideinject,
    Computed,
    CreatePosts,
    VModel,
    PostList,
    TemplateRef,
    HoverCounter,
    ClickCounter, 
    DemoTwo,
    DemoOne,
    Data,
    Methods,
  },
  data(){
    return {
     name:"Vite App",
    }
  },
}
</script>

<template>
 <HoverCounter />
 <ClickCounter />
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
