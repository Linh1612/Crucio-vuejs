<template>
  <div class="body-content10">
    <div class="title-btn">
      <h2 class="leftToCenter">WANT TO DISCUSS YOUR NEW PROJECT?</h2>
      <button class="bottomToTop">CONTACT US</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body-content10 {
  height: 25rem;
  background-color: var(--primary-color);
  margin-top: 1rem;
  padding: 10rem;
  text-align: center;
  color: white;
  letter-spacing: 5px;
  font-size: 1rem;
}

.body-content10 > .title-btn h2 {
  font-weight: 100;
  padding-bottom: 3rem;
}

.body-content10 > .title-btn button {
  width: 12.5rem;
  height: 3rem;
  background-color: var(--primary-color);
  border: 3px solid white;
  color: white;
  font-size: 1rem;
  letter-spacing: 2px;
  cursor: pointer;
}

.body-content10 > .title-btn button:hover {
  background-color: white;
  color: var(--primary-color);
  transition: 1s;
}
</style>
