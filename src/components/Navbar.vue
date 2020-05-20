<template>
  <div>
    <b-nav class="nav text-light">
      <ul class="nav">
        <li class="nav-item">

          <router-link to="/" class="nav-link active">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="nav-link active">About</router-link>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" href="#">Deck Builder</a>
        </li>
      </ul>
    </b-nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.nav {
  background-color: #1d1025;
}
a {
  color: white;
  font-size: 2rem;
}
</style>
