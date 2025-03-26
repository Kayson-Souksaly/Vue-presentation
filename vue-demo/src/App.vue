<script setup>
import ComputedBtn from './components/ComputedBtn.vue'
import ListRenderBtn from './components/ListRenderBtn.vue'
import ReactiveBtn from './components/ReactiveBtn.vue'
import RefBtn from './components/RefBtn.vue'
import VIfElseBtn from './components/VIfElseBtn.vue'
</script>

<template>
  <main>
    <section class="container py-5">
      <div class="header-wrapper">
        <img alt="Vue logo" class="logo" src="./assets/logo.svg" />

        <div class="wrapper">
          <h1 class="green mb-5">Welcome to Vue Feature Demo!</h1>
        </div>
      </div>

      <!-- Ref() -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">Declaring Reactive State Part 1</h1>
          <h2>ref()</h2>
          <p>ref() takes the argument and returns it wrapped within a ref object</p>
        </div>
        <div class="card-body">
          <RefBtn />
        </div>
      </div>

      <!-- Reactive() -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">Declaring Reactive State Part 2</h1>
          <h2>reactive()</h2>
          <p>reactive() creates a reactive object from an object or array</p>
        </div>
        <div class="card-body">
          <ReactiveBtn />
        </div>
      </div>

      <!-- Computed Properties -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">Computed Properties</h1>
          <h2>computed()</h2>
          <p>Creates derived state that updates automatically when dependencies change</p>
        </div>
        <div class="card-body">
          <ComputedBtn />
        </div>
      </div>

      <!-- Conditional Rendering -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">Conditional Rendering</h1>
          <h2>v-if</h2>
          <p>
            The directive v-if is used to conditionally render a block. <br />
            The block will only be rendered if the directive's expression returns a truthy value.
          </p>
        </div>
        <div class="card-body">
          <VIfElseBtn />
        </div>
      </div>

      <!-- List Rendering -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">List Rendering</h1>
          <h2>v-if</h2>
          <p>
            The directive v-if is used to conditionally render a block. <br />
            The block will only be rendered if the directive's expression returns a truthy value.
          </p>
        </div>
        <div class="card-body">
          <ListRenderBtn />
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.header-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
body {
  display: flex;
  flex-direction: column;
}

header {
  line-height: 1.5;
}

section {
  padding: 10vh 0 10vh 0;
  text-align: center;
}

.header {
  padding-bottom: 4vh;
}

.header p,
.card-body {
  font-size: 1.5em;
  padding: 2vh;
}

@media (min-width: 1024px) {
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
}

.logo {
  height: 20vh;
  width: auto;
}
</style>
