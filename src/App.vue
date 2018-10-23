<template>
  <div id="app" class="bg-purple-light">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
@tailwind preflight;
@tailwind components;
@tailwind utilities;
</style>
