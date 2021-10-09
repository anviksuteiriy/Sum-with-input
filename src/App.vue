<template>
  <div>
    <div>
      <div class="mb-2 text-2xl font-bold">Add Two Numbers</div>
      <ComInput
        v-model:value="a"
        class=""
        aria-label="A"
        placeholder="A"
      />
      <ComInput
        v-model:value="b"
        class="mt-3 mb-3"
        aria-label="B"
        placeholder="B"
      />
      <button :disabled="buttonDisable" @click="calculate" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Click me
      </button>
      <p class="mt-2 text-2xl font-bold">{{sum}}</p>
    </div>
  </div>
</template>

<script>
import './assets/tailwind.css';
import ComInput from './components/ComInput.vue';
export default {
  components: {
    ComInput
  },
  name: 'App',
  data() {
    return {
      a: undefined,
      b: undefined,
      sum: undefined
    }
  },
  computed: {
    buttonDisable() {
      return !this.a || !this.b
    }
  },
  methods: {
    calculate() {
      this.sum = parseFloat(this.a) + parseFloat(this.b);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
