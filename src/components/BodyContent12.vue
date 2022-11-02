<template>
  <div class="body-content12">
    <div class="img-logo">
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client1-150x150.png"
        alt="logo"
      />
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client2-150x150.png"
        alt="logo"
      />
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client3-132x150.png"
        alt="logo"
      />
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client4.png"
        alt="logo"
      />
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client5.png"
        alt="logo"
      />
      <img
        src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client6.png"
        alt="logo"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body-content12 {
  height: 12.5rem;
  background-color: var(--light-color);
}

.body-content12 > .img-logo {
  display: flex;
  justify-content: space-around;
  padding: 4rem 10rem;
}

.body-content12 > .img-logo img {
  width: 5rem;
  height: 4rem;
  opacity: 0.6;
  cursor: pointer;
}

.body-content12 > .img-logo img:hover {
  opacity: 1;
  transition: 1s;
}
</style>
