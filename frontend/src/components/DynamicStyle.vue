<template>
    <header>
      <h1>Vue Dynamic Styling</h1>
    </header>
    <section id="styling">
      <div
          @click="selectedBox('A')"
          :class="boxA ? 'demo active' : 'demo'"></div>
      <div
          @click="selectedBox('B')"
          class="demo"
          :class="['demo', {active: boxB}]"
      ></div>
      <div
          @click="selectedBox('C')"
          class="demo"
          :class="boxCSelected"
      ></div>
    </section>
</template>

<script>
export default {
  name: "DynamicStyle",
  data() {
    return {
     boxA: false,
     boxB: false,
     boxC: false,
    }
  },
  computed: {
    boxCSelected() {
      return {active: this.boxC}
    }
  },
  methods: {
    selectedBox(name) {
      if (name === 'A') {
        return this.boxA = !this.boxA
      } else  if (name === 'B') {
        return this.boxB = !this.boxB
      } else  if (name === 'C') {
        return this.boxC = !this.boxC
      }
    }
  }
}
</script>

<style scoped>
* {
  box-sizing: border-box;
}

html {
  font-family: 'Jost', sans-serif;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: #4fc08d;
  color: white;
  text-align: center;
}

#styling {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

.demo {
  width: calc(100% - 32px);
  height: 100px;
  margin: 16px;
  border: 2px dashed #ccc;
}
.active {
  border-color: red;
  background-color: salmon;
}
</style>