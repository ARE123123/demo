<template>
  <div id="three" class="container"></div>
</template>

<script setup>
import * as THREE from 'three';
import * as maptalks from 'maptalks';
import { ThreeLayer } from 'maptalks.three';
import { onMounted } from 'vue';

onMounted(() => {
  var map = new maptalks.Map('three', {
    center: [-0.113049, 51.498568],
    zoom: 14,
    baseLayer: new maptalks.TileLayer('base', {
      urlTemplate: 'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}.png',
      subdomains: ['a', 'b', 'c', 'd'],
      attribution:
        '&copy; <a href="http://osm.org">OpenStreetMap</a> contributors, &copy; <a href="https://carto.com/">CARTO</a>',
    }),
  });
});
</script>

<style>
html,
body {
  margin: 0px;
  height: 100%;
  width: 100%;
}

#app,
.container {
  width: 100%;
  height: 100%;
}
</style>
