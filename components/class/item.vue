<template>
  <nuxt-link class="card w-100" to="/class/frontEnd">
    <img src="~/assets/img/pc_gaming.jpg" class="card-img-top img-thumbnail" alt="class IT Support">
    <div class="card-body">
      <p class="card-text">{{desc}}</p>
    </div>
  </nuxt-link>
</template>
<script>
export default {
  props: {
    desc: {
      type: String,
      default: "IT Support",
    },
    id: {
      type: Number,
      default: 1,
    },
  },
};
</script>