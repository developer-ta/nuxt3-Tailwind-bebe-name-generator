<script setup lang="ts">
enum Gender {
  GIRL = "Girl",
  BOY = "Boy",
  UNISEX = "Unisex",
}
enum Popularity {
  TRENDY = "Trendy",
  UNIQUE = "Boy",
}
enum Length {
  SHORT = "Short",
  LONG = "Long",
  ALL = "All",
}
interface OptionState {
  gender: Gender;
  popularity: Popularity;
  length: Length;
}
const data_options: OptionState = reactive({
  gender: Gender.GIRL,
  popularity: Popularity.TRENDY,
  length: Length.SHORT,
});
const titleClass = {
  "text-red-400": !"true",
  "text-gray-500": "true",
};
</script>

<template>
  <main class="container flex flex-col prose bg-indigo-50 h-auto w-[100%]">
    <section class="mt-8">
      <h1>Baby Name Generator</h1>
      <p>Choose your options and click the "Find Names" bottom below</p>
      <div :class="titleClass">Hello World</div>
    </section>

    <section
      class="options-container bg-gradient-to-tr from-rose-200 to-violet-300 rounded-3xl p-4 shadow-md shadow-blue-900 mt-16 mb-8 relative m-[2%]"
    >
      <div class="option-container">
        <h3>1) Choose a gender</h3>
        <div class="option-buttons">
          <button
            class="btn-primary"
            :class="data_options.gender === Gender.BOY && 'option-active'"
          >
            Boy
          </button>
          <button
            class="btn-primary"
            :class="data_options.gender === Gender.UNISEX && 'option-active'"
          >
            Unisex
          </button>

          <button
            class="btn-primary"
            :class="data_options.gender === Gender.GIRL && 'option-active'"
          >
            Girl
          </button>
        </div>
      </div>
      <div class="option-container">
        <h3>2) Choose the name's popularity</h3>
        <div class="option-buttons">
          <button
            class="btn-primary"
            :class="data_options.popularity === Popularity.TRENDY && 'option-active'"
          >
            Trendy
          </button>
          <button
            class="btn-primary"
            :class="data_options.popularity === Popularity.UNIQUE && 'option-active'"
          >
            Unique
          </button>
        </div>
      </div>
      <div class="option-container">
        <h3>3) Choose name's length</h3>
        <div class="option-buttons">
          <button
            class="btn-primary"
            :class="data_options.length === Length.LONG && 'option-active'"
          >
            Long
          </button>
          <button
            class="btn-primary"
            :class="data_options.length === Length.ALL && 'option-active'"
          >
            All
          </button>
          <button
            class="btn-primary"
            :class="data_options.length === Length.SHORT && 'option-active'"
          >
            Short
          </button>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.option-active {
  @apply bg-red-600 text-white ring-red-400 ring-2;
}

.root {
  @apply container w-96 mx-auto my-0 mt-1 rounded-2xl p-1;
}

input {
  @apply border-0 outline-0 border-b-2 border-solid border-red-200 rounded text-base w-[99%] py-1;
  margin: 10px 0 5px 0;
}

button {
  @apply btn-primary;
}
</style>
