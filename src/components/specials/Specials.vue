<script setup>
import { specials } from "../../store/useRestaurant";
</script>

<template>
  <!-- Specials -->
  <div class="specials p-5" id="specials">
    <div class="container">
      <div class="grid">
        <div class="row mt-5">
          <div
            class="col-md-4 text-center"
            v-for="special in specials"
            :key="special.id"
          >
            <i class="fa fa-4x" :class="special.icon"></i>
            <p class="h2 dance-font fw-bold my-2">{{ special.name }}</p>
            <p class="lead fst-italic">
              {{ special.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>