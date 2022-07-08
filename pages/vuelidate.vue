<template>
  <div class="root">
    <h2>Create an Account</h2>
    <p>
      <input type="text" placeholder="email" />
    </p>
    <p>
      <input type="password" placeholder="Password" />
    </p>
    <p>
      <input type="text" placeholder="Confirm Password" />
    </p>
    <button>submit</button>
  </div>
</template>

<script setup></script>

<style scoped>
.root {
  @apply container w-96 mx-auto my-0 mt-24 rounded-2xl p-7;
}

input {
  @apply border-0 outline-0 border-b-2 border-solid border-red-200 text-base w-[99%] py-1;
  margin: 10px 0 5px 0;
}

button {
  @apply btn-primary;
}
</style>
