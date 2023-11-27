<script lang="ts" setup></script>
<template>
  <nav class="bg-gray-900 text-white py-5 border-b border-gray-700">
    <div
      class="container flex flex-col sm:flex-row justify-center gap-3 sm:gap-0 sm:justify-between items-center"
    >
      <NuxtLink to="/" class="text-2xl font-medium">SHV Blog</NuxtLink>
      <ul class="nav">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/categories">Categories</NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

