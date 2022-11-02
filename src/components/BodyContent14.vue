<template>
  <div class="body-content14">
    <div>
      <a href="#logo"
        ><img
          src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/05/logo-1.png"
          alt="logo"
      /></a>
    </div>
    <div class="info-task">
      <ul>
        <li>
          <a href="#facebook"
            ><iconify-icon icon="bxl:facebook-square"></iconify-icon
          ></a>
        </li>
        <li>
          <a href="#twitter"
            ><iconify-icon icon="akar-icons:twitter-fill"></iconify-icon
          ></a>
        </li>
        <li>
          <a href="#instagram"
            ><iconify-icon icon="akar-icons:instagram-fill"></iconify-icon
          ></a>
        </li>
        <li>
          <a href="#linkedin"
            ><iconify-icon icon="akar-icons:linkedin-box-fill"></iconify-icon
          ></a>
        </li>
        <li>
          <a href="#dribbble"
            ><iconify-icon icon="akar-icons:dribbble-fill"></iconify-icon
          ></a>
        </li>
        <li>
          <a href="#youtube"
            ><iconify-icon icon="akar-icons:youtube-fill"></iconify-icon
          ></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body-content14 {
  background-color: rgb(1, 1, 1);
  height: 15rem;
  margin-top: 20rem;
  padding: 0 10rem;
  padding-top: 3rem;
  text-align: center;
}

.body-content14 div {
  padding-bottom: 2rem;
}

.body-content14 > .info-task {
  text-align: center;
}

.body-content14 > .info-task ul {
  display: flex;
  color: white;
  list-style: none;
  justify-content: center;
}

.body-content14 > .info-task li {
  padding-left: 3rem;
}

.body-content14 > .info-task ul li a {
  color: white;
}

.body-content14 > .info-task ul li a iconify-icon {
  font-size: 1.8rem;
}

.body-content14 > .info-task ul li a:hover {
  color: var(--primary-color);
  transition: 1s;
}
</style>
