<script setup lang="ts">
window.addEventListener("click", (e) => {
  if (e.target != document.querySelector(".fa-bars")) {
    console.log(e.target);
  }
});
</script>
<template>
  <div class="navbar">
    <div class="bot-name">bot-name</div>
    <div class="menu"><div class="link">Dashboard</div></div>
    <i class="fa-solid fa-bars"></i>
  </div>
</template>
<style scoped>
.navbar {
  background-color: var(--navbar-bg-color);
  height: 40px;
  display: flex;
  align-items: center;
  padding: 0 20px;
  justify-content: space-between;
}
.bot-name {
  text-transform: uppercase;
  color: white;
  font-family: "Roboto", sans-serif;
  font-weight: bold;
}
.link {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  color: var(--navbar-item-color);
}
.fa-bars {
  display: none;
  cursor: pointer;
  color: var(--menu-bar-color);
  font-size: var(--menu-bar-font-size);
  transition: color 0.2s ease-in-out;
}
.fa-bars:hover {
  color: var(--menu-bar-hover-color);
}
@media screen and (max-width: 768px) {
  .fa-bars {
    display: block;
  }
}
</style>
