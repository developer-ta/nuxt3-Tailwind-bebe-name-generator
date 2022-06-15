<script setup>
const data_options = reactive({});
</script>

<template>
  <main class="container flex flex-col justify-center prose">
    <h1>Baby Name Generator</h1>
    <p>Choose your options and click the "Find Names" bottom below</p>
    <section
      class="options-container bg-gradient-to-tr from-rose-200 to-violet-300 rounded-3xl p-4 shadow-md shadow-blue-900 mt-16 mb-8 relative m-[2%]"
    >
      <div class="option-container">
        <h4>1) Choose a gender</h4>
        <div class="option-buttons">
          <button class="btn-primary">Boy</button>
          <button class="btn-primary">Unisex</button>

          <button class="btn-primary">Girl</button>
        </div>
      </div>
      <div class="option-container">
        <h4>2) Choose the name's popularity</h4>
        <div class="option-buttons">
          <button class="btn-primary">Trendy</button>
          <button class="btn-primary">Unique</button>
        </div>
      </div>
      <div class="option-container">
        <h4>2) Choose name's length</h4>
        <div class="option-buttons">
          <button class="btn-primary">Long</button>
          <button class="btn-primary">All</button>
          <button class="btn-primary">Short</button>
        </div>
      </div>
    </section>
  </main>
</template>
