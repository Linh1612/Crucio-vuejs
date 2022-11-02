<template>
  <div id="about" class="body-content2">
    <div>
      <h2>WELCOME TO <strong class="color">CRUCIO</strong></h2>
      <h3>WE CREATE AWESOME WEBSITES</h3>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
        tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea
        commodi consequat. Quis aute iure reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat
        cupiditat non proident, sunt in culpa qui officia deserunt mollit anim
        id est laborum.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body-content2 {
  text-align: center !important;
  height: 40rem;
}

.body-content2 div {
  padding-top: 15rem;
}

.body-content2 div h2 {
  letter-spacing: 10px;
  font-size: 3rem;
  font-weight: 300;
}

.color {
  color: var(--primary-color);
}

.body-content2 div h3 {
  padding-top: 2rem;
  letter-spacing: 10px;
  font-size: 2rem;
}

.body-content2 div p {
  padding-top: 3rem;
  text-align: center;
  padding-left: 10rem;
  padding-right: 10rem;
  font-size: 14px;
  line-height: 1.8;
  color: var(--text-color);
  letter-spacing: 1px;
}
</style>
