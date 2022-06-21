<template>
  <div id="app">
    <keep-alive exclude="Detail"> <router-view /></keep-alive>
  </div>

  <!-- <router-view v-slot="{ Component }">
    <keep-alive>
      <component :is="Component" />
    </keep-alive>
  </router-view> -->
</template>
