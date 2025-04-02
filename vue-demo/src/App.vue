<script setup>
import ComputedBtn from './components/ComputedBtn.vue'
import FormBinding from './components/FormBinding.vue'
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
          <p>
            Demonstrates Vue's <code>ref()</code> function for creating a reactive primitive value.
            This example shows how clicking a button updates the displayed text reactively.
          </p>
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
          <p>
            Uses <code>reactive()</code> to manage a reactive object containing user information.
            Clicking a button extracts and displays individual properties using reactivity.
          </p>
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
          <p>
            Showcases <code>computed()</code> to derive values based on reactive state. It
            dynamically updates the answer based on the length of a task list.
          </p>
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
            Illustrates conditional rendering using <code>v-if</code>, <code>v-else-if</code>, and
            <code>v-else</code>. Selecting an animal from buttons displays the corresponding image.
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
          <h2>v-for</h2>
          <p>
            This section demonstrates how to use <code>v-for</code> to dynamically render a list of
            items from a reactive array. This showcases Vue’s reactivity in action.
          </p>
        </div>
        <div class="card-body">
          <ListRenderBtn />
        </div>
      </div>

      <!-- Form Input Bindings -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">Form Input Bindings and Event Handler</h1>
          <h2>v-model</h2>
          <p>
            This example demonstrates how to bind form inputs to reactive data using
            <code>v-model</code> and respond to user interaction with event listeners like
            <code>@click</code> and <code>@keyup.enter</code>. It checks the user’s answer to a
            simple math problem and gives real-time feedback using conditional rendering.
          </p>
        </div>
        <div class="card-body">
          <FormBinding />
        </div>
      </div>

      <!-- In-Class Coding -->
      <div class="card mb-5">
        <div class="header">
          <h1 class="green card-header">In-Class Coding</h1>
          <h2>Task</h2>
          <p>
            Build a fully functional Calculator App with addition, subtraction, multiplication, and
            division capability using:
          </p>
          <div class="list-container w-100">
            <ul class="w-50">
              <li><code>ref()</code> for reactive state</li>
              <li><code>v-model</code> for two input fields</li>
              <li><code>@click</code> for addition, subtraction, multiplication, and division</li>
              <li>
                <span class="text-danger">Bonus: </span>Use <code>v-if</code> to check if result is
                odd or even
              </li>
            </ul>
          </div>
        </div>
        <div class="card-body">
          <p class="text-info">Download Template Code Here</p>
          <a
            href="https://github.com/Kayson-Souksaly/Vue-ClassDemo"
            target="_blank"
            class="btn btn-success"
            >Click Here!</a
          >

          <p class="text-info mt-4">View Completed Calculator</p>
          <a
            href="https://vue-calculator-0g6r.onrender.com/"
            target="_blank"
            class="btn btn-success"
          >
            Calculator App
          </a>
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

code {
  font-size: 1.2em;
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

.list-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

ul {
  text-align: left;
  font-size: 1.5em;
}

.logo {
  height: 20vh;
  width: auto;
}
</style>
