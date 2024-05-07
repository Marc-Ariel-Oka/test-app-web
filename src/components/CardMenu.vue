<script>
export default {
  props: ["img", "name", "isService"],
};
</script>

<template>
  <div class="d-flex flex-column align-items-center">
    <div
      class="py-3 px-3 card-menu d-flex justify-content-center align-items-center mb-2" :class="isService ? 'img' : ''"
    >
      <img
        :src="`src/assets/icons/${img}`"
        alt=""
        
      />
    </div>
    <p
      style="
        font-size: 12px;
        font-weight: 500;
        line-height: 16px;
        letter-spacing: 0.5px;
        width: 100%;
        text-align: center;
      "
    >
      {{ name }}
    </p>
  </div>
</template>

<style scoped>
.card-menu {
  background-color: #eeeeee;
  border-radius: 15px;
  width: 100%;
}
.card-menu img {
  height: 50px;
  width: 50px;
  object-fit: contain;
}

.img img {
  height: 40px;
  width: 40px;
  object-fit: contain;
}
</style>
