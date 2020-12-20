<template>
  <div class="card">
    <div class="card-header ">
      <h5 class="card-title text-center">{{ member.nombre }}</h5>
    </div>
    <div class="pt-1 pl-2 pr-5 ">
      <img
          :src="member.image"
        alt=""
        height="300"
        class="card-img rounded-circle border border-dark"
      />
    </div>
    <div class="card-body ">
      <p class="card-text text-center">{{ member.descripcion }}</p>
      <ul class="list-group list-group-flush ">
        <li class="list-group-item bg-secondary text-white"><b>Rol:</b> {{ member.rol }}</li>
        <li class="list-group-item bg-secondary text-white"><b>Codigo: </b> {{ member.codigo }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>
</style>
