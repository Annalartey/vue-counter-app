<template>
  <p>Count is: {{ count }} </p>
  <button @click="increaseCount">increase</button>
  <button @click="decreaseCount">decrease</button>
  <button @click="resetCount">Reset</button>

  <div>
    <input type="number" />
    <button>Set Value</button>
  </div>
</template>

<script>
  export default {
    name: "Counter",
    data () {
    return{
      count: 0,
    }
  },
    methods : {
    increaseCount () {
      console.log("increased")
      this.count++;
    },
    decreaseCount () {
      console.log("decreased")
      this.count--;
    },
    resetCount () {
      console.log("reset")
      this.count = 0;
    },
    },
  }
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
