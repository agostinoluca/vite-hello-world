<script>
export default {
  name: 'App',
  data(){
    return {
      type: 'button',
      link: 'this is a link',
      name: '',
      surname: '',
      count: 0
    }
  },
  methods: {
    testFunction(){
      console.log('Sto testando methods');
      this.testFunction2();
      this.testFunction3();
    },
    testFunction2(){
      console.log('Funziono?');
    },
    testFunction3(){
      this.count++;
    }
  }
};
</script>

<template>
<header>
  <h1>Hello World</h1>
</header>
<!-- /header -->

<main>
  <div class="inputTest">
    <label for="name">Name</label>
    <input type="text" v-model="name">

    <label for="surname">Surname</label>
    <input type="text" v-model="surname">

  </div>
  <button @click="testFunction">
    <p>Hello {{ name + ' ' + surname }}</p>
    <p>You click this {{ type }} {{ count }} times</p>
  </button>
</main>
<!-- /main -->

<footer>
  <ul class="test">
    <li><a href="#">{{ link }}</a></li>
    <li><a href="#">{{ link }}</a></li>
    <li><a href="#">{{ link }}</a></li>
    <li><a href="#">{{ link }}</a></li>
    <li><a href="#">{{ link }}</a></li>
  </ul>
</footer>
<!-- /footer -->
</template>

<style>
</style>
