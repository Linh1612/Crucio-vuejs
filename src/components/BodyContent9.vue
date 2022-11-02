<template>
  <div class="body-content9">
    <h3 class="topToBottom">Subscribe To Our Newsletter</h3>
    <form action="#">
      <input
        class="input-text"
        type="text"
        placeholder="Enter your email..."
        name="gmail"
      /><br />
      <input
        class="input-submit"
        type="submit"
        name="Subscribe"
        value="SUBSCRIBE"
      />
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body-content9 {
  height: 25rem;
  padding: 7rem;
  text-align: center;
  letter-spacing: 5px;
  font-size: 1.5rem;
}

.body-content9 h3 {
  font-weight: 100;
  padding-bottom: 3rem;
}

.body-content9 form > .input-text {
  border: 0;
  border-bottom: 1px solid rgba(30, 30, 30, 0.3);
  visibility: visible;
  animation-duration: 1s;
  animation-delay: 0.5s;
  animation-name: fadeInLeft;
  padding: 5px;
  width: 60%;
  text-align: center;
  font-size: 1rem;
}

.body-content9 form input:focus {
  outline: none;
}

.body-content9 form > .input-submit {
  margin-top: 3rem;
  background-color: white;
  border: 3px solid var(--primary-color);
  padding: 0.75rem 1.25rem;
  color: var(--primary-color);
  letter-spacing: 3px;
  font-size: 1rem;
}

.body-content9 form > .input-submit:hover {
  background-color: var(--primary-color);
  color: white;
  transition: 1s;
}
</style>
