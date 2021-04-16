<template>
  <div>
    <PartialsTitle title="MyClass" /> 
    <div class="row">
      <div class="col-sm-4" v-for="(item,i) in listClass" :key="i">
        <class-item :desc="item.desc" :id="i"/>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      listClass: [
        { desc: "IT Support"},
        { desc: "Full Stack Devlopmet"},
        { desc: "Front End Devopment"},
        { desc: "Back End Devlopment"},
      ],
    };
  },
}
</script>