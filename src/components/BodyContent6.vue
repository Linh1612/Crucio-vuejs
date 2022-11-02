<template>
  <div id="team" class="body-content6">
    <div class="text-center">
      <h2>OUR TEAM</h2>
      <hr />
    </div>
    <div class="team">
      <div
        :class="content6Item.parent"
        v-for="content6Item in content6Items"
        :key="content6Item.id"
      >
        <div :class="content6Item.father">
          <h2 class="topToBottom">{{ content6Item.name }}</h2>
          <p class="bottomToTop">{{ content6Item.role }}</p>
          <div :class="content6Item.children">
            <ul>
              <li>
                <iconify-icon :icon="content6Item.icon1"></iconify-icon>
              </li>
              <li>
                <iconify-icon :icon="content6Item.icon2"></iconify-icon>
              </li>
              <li>
                <iconify-icon :icon="content6Item.icon3"></iconify-icon>
              </li>
              <li>
                <iconify-icon :icon="content6Item.icon4"></iconify-icon>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content6Items: [
        {
          id: 61,
          parent: "bg-1 leftToCenter",
          father: "person-info",
          name: "SAMANTA L.",
          role: "Architect",
          children: "info",
          icon1: "bxl:facebook-square",
          icon2: "akar-icons:twitter-fill",
          icon3: "akar-icons:instagram-fill",
          icon4: "akar-icons:linkedin-box-fill",
        },
        {
          id: 62,
          parent: "bg-2 topToBottom",
          father: "person-info",
          name: "PAMELA K.",
          role: "Designer",
          children: "info",
          icon1: "bxl:facebook-square",
          icon2: "akar-icons:twitter-fill",
          icon3: "akar-icons:instagram-fill",
          icon4: "akar-icons:linkedin-box-fill",
        },
        {
          id: 63,
          parent: "bg-3 rightToCenter",
          father: "person-info",
          name: "MICHEAL J.",
          role: "Planner",
          children: "info",
          icon1: "bxl:facebook-square",
          icon2: "akar-icons:twitter-fill",
          icon3: "akar-icons:instagram-fill",
          icon4: "akar-icons:linkedin-box-fill",
        },
      ],
    };
  },
};
</script>

<style scoped>
.body-content6 {
  height: 60rem;
  text-align: center;
}

.body-content6 > .text-center h2 {
  padding-top: 12.5rem;
  letter-spacing: 5px;
  font-family: "Open Sans", sans-serif;
  font-size: 2rem;
  font-weight: 200;
  padding-bottom: 1rem;
}

.body-content6 > .text-center hr {
  width: 3rem;
  height: 3px;
  margin: 0 auto;
  background-color: rgb(173, 0, 255);
  border: none;
  margin-bottom: 2rem;
}

.body-content6 > .team {
  display: flex;
  padding: 0 15rem;
}

.body-content6 > .team > .bg-1 {
  width: 33.3%;
  height: 25rem;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team1.jpg");
  max-width: 400px;
  max-height: 600px;
}

.body-content6 > .team > .bg-2 {
  width: 33.3%;
  height: 25rem;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team2.jpg");
  max-width: 400px;
  max-height: 600px;
  margin: 0 5rem;
}

.body-content6 > .team > .bg-3 {
  width: 33.3%;
  height: 25rem;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team3.jpg");
  max-width: 400px;
  max-height: 600px;
}

.person-info {
  padding-top: 10rem;
  background-color: var(--primary-color);
  height: 100%;
  opacity: 0;
  cursor: pointer;
  color: white;
}

.person-info > p {
  padding-bottom: 2rem;
}

.person-info > .info > ul {
  list-style: none;
}

.person-info > .info > ul > li {
  display: inline-block;
  padding: 0 1rem;
}

.body-content6 > .team > .bg-1:hover .person-info,
.body-content6 > .team > .bg-1:focus .person-info {
  opacity: 0.8;
  transition: ease-in 1s;
}

.body-content6 > .team > .bg-2:hover .person-info,
.body-content6 > .team > .bg-2:focus .person-info {
  opacity: 0.8;
  transition: ease-in 1s;
}

.body-content6 > .team > .bg-3:hover .person-info,
.body-content6 > .team > .bg-3:focus .person-info {
  opacity: 0.8;
  transition: ease-in 1s;
}
</style>
