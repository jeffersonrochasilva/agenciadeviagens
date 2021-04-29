<template>
  <header>
    <div class="logo">
      <h1>NPM Viagens</h1>
    </div>
    <Nav />
  </header>
</template>
<script>
import Nav from "@/components/Nav";

export default {
  components: {
    Nav
  }
};
</script>

<style scoped>
header {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  width: 400px;
}
</style>
