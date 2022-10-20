<script setup>
import { chefs } from "../../store/useRestaurant";
import ChefCard from "../chefs/ChefCard.vue";

const showLink = (link) => {
  //const alpha = chefs[link[1]];
  //alert(alpha[link[0]]);
  alert(chefs[link[1]][link[0]]);
};
//https://www.youtube.com/watch?v=9whgkjxoCME&t=1254s
//https://www.youtube.com/watch?v=kCo0re40Aao
</script>

<template>
  <!-- Chefs -->
  <section class="chefs p-5" id="chefs">
    <div class="container">
      <div class="grid">
        <div class="row mt-5">
          <!-- x -->
          <div class="col-md-3" v-for="chef in chefs" :key="chef.id">
            <ChefCard
              :id="chef.id"
              :media="chef.media"
              :name="chef.name"
              :title="chef.title"
              :describe="chef.describe"
              @buttonclicked="showLink"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>