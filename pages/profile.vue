<template>
  <div>
    <PartialsTitle title="My Profile" />
    <h1>profile</h1>
  </div>
</template>
<script>
export default {
  created() {
    console.log(this.$route);
  },
};
</script>
