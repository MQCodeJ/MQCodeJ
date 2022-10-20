<script setup>
import { menus } from "../../store/useRestaurant";
import MenuTextLeft from "../menus/MenuTextLeft.vue";
import MenuTextRight from "../menus/MenuTextRight.vue";

// id is even (true) or odd (false) number
const isTextInTheLeft = (number) => {
  return number % 2 == 0;
};
</script>
  
<template>
  <!-- Menus Section -->
  <section class="menus">
    <div v-for="menu in menus" :key="menu.id">
      <MenuTextLeft
        :chapter="menu.chapter"
        :title="menu.title"
        :description="menu.description"
        :mediasrc="menu.mediasrc"
        :mediatype="menu.mediatype"
        v-if="isTextInTheLeft(menu.id)"
      />
      <MenuTextRight
        :chapter="menu.chapter"
        :title="menu.title"
        :description="menu.description"
        :mediasrc="menu.mediasrc"
        :mediatype="menu.mediatype"
        v-else
      />
    </div>
  </section>
</template>