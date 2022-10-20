<script setup>
const props = defineProps({
  id: Number,
  media: String,
  name: String,
  title: String,
  describe: String,
});

const emit = defineEmits(["buttonclicked"]);
</script>

<template>
  <div class="card shadow-lg my-2">
    <img :src="media" :alt="id" class="img-fluid" />
    <div class="card-body">
      <p class="h4 card-title fw-bold">{{ name }}</p>
      <p class="dance-font text-muted">{{ title }}</p>
      <p class="fst-italic">{{ describe }}</p>
      <div class="d-flex justify-content-around">
        <div class="pointer" @click="$emit('buttonclicked', ['faceb', id])">
          <i class="fab fa-facebook text-primary fa-2x"></i>
        </div>
        <div class="pointer" @click="$emit('buttonclicked', ['twitt', id])">
          <i class="fab fa-twitter text-info fa-2x"></i>
        </div>
        <div class="pointer" @click="$emit('buttonclicked', ['ytube', id])">
          <i class="fab fa-youtube text-danger fa-2x"></i>
        </div>
        <div class="pointer" @click="$emit('buttonclicked', ['insta', id])">
          <i class="fab fa-instagram text-warning fa-2x"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.pointer {
  cursor: pointer;
}
</style>