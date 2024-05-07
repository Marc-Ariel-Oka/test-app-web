<script>
export default {
  data() {
    return {
      menu: [
        {
          img: "atom_primaryicon_grid_filled.png",
          name: "Welcome",
          isActive: true,
        },
        { img: "icon-container.png", name: "Marketplace", isActive: false },
        { img: "icon-container-1.png", name: "Mobile", isActive: false },
        { img: "icon-container-2.png", name: "My wallet", isActive: false },
        { img: "icon-container-3.png", name: "My points", isActive: false },
      ],
    };
  },
};
</script>

<template>
  <div
    class="sticky-bottom px-3 d-flex justify-content-center align-items-center text-center"
    style="min-height: 10vh; background-color: #fafafa"
  >
    <div
      class="bottom-item d-flex flex-column align-items-centerg me-auto"
      v-for="row in menu"
    >
      <img
        :src="`src/assets/icons/Building Blocks/${row.img}`"
        alt=""
        class=" mb-2"
        :class="row.isActive ? 'menuActive px-4 py-1 rounded-5' : ''"
      />
      <p style="color: #1c1b1f; font-weight: 500; font-size: 11px">
        {{ row.name }}
      </p>
    </div>
  </div>
</template>

<style scoped>
.menuActive {
  background-color: #eeeeee;
}
</style>
