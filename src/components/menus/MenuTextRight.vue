<script setup>
const props = defineProps({
  chapter: String,
  title: String,
  description: String,
  mediasrc: String,
  mediatype: String,
});
</script>

<template>
  <div class="menu-2 bg-white p-5">
    <div class="container">
      <div class="grid">
        <div class="row align-items-center">
          <div class="col-md-6">
            <video controls autoplay class="img-fluid">
              <source :src="props.mediasrc" :type="props.mediatype" />
            </video>
          </div>
          <div class="col-md-6">
            <p class="h2 dance-font fw-bold">
              {{ props.chapter }}
              <span class="text-warning">{{ props.title }}</span>
            </p>
            <p class="lead fst-italic">{{ props.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
