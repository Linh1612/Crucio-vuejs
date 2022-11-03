<template>
  <div id="portfolio" class="body-content8">
    <div class="text-center">
      <h2>OUR PORTFOLIO</h2>
      <hr />
    </div>
    <!-- <div class="taskbar">
      <ul>
        <li><a href="#all" @click="type = 'all'">All</a></li>
        <li><a href="#graphicDesign">Graphic Design</a></li>
        <li><a href="#webDesign">Web Design</a></li>
        <li><a href="#webDevelopment">Web Development</a></li>
      </ul>
    </div> -->
    <div className="taskbar">
      <ul>
        <li v-for="(item, index) in listTag" :key="index">
          <a :href="'#' + item" @click="type = item"> {{ titleTag[index] }} </a>
        </li>
      </ul>
    </div>
    <div class="works" v-if="onShow() && show">
      <div
        :class="content8Items[index].parent"
        v-for="index in detailImg[type]"
        :key="index"
      >
        <div :class="content8Items[index].father">
          <div :class="content8Items[index].children">
            <h2>{{ content8Items[index].headline }}</h2>
            <p>{{ content8Items[index].paragraph }}</p>
          </div>
        </div>
      </div>
      <div v-if="!hidden" :class="content8Items[8].parent">
        <div :class="content8Items[8].father">
          <div :class="content8Items[8].children">
            <h2>{{ content8Items[8].headline }}</h2>
            <p>{{ content8Items[8].paragraph }}</p>
          </div>
        </div>
      </div>
    </div>
    <div v-if="hidden" class="bg-btn">
      <button @click="hidden = !hidden" class="btn">LOAD MORE</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      type: "all",
      show: false,
      listTag: ["all", "graphicDesign", "webDesign", "webDevelopment"],
      titleTag: ["All", "Graphic Design", "Web Design", "Web Development"],
      windowTop: 0,
      hidden: true,
      moreImg: [8],
      detailImg: {
        all: [0, 1, 2, 3, 4, 5, 6, 7],
        graphicDesign: [2, 5, 6, 7],
        webDesign: [0, 3, 4, 5, 6],
        webDevelopment: [1, 3],
      },
      content8Items: [
        {
          id: 81,
          parent: "work-1 rightToCenter",
          father: "bg-1",
          children: "work-info",
          headline: "Project #1",
          paragraph: "Project Description",
        },
        {
          id: 82,
          parent: "work-2 rightToCenter",
          father: "bg-2",
          children: "work-info",
          headline: "Project #2",
          paragraph: "Project Description",
        },
        {
          id: 83,
          parent: "work-3 rightToCenter",
          father: "bg-3",
          children: "work-info",
          headline: "Project #3",
          paragraph: "Project Description",
        },
        {
          id: 84,
          parent: "work-4 rightToCenter",
          father: "bg-4",
          children: "work-info",
          headline: "Project #4",
          paragraph: "Project Description",
        },
        {
          id: 85,
          parent: "work-5 rightToCenter",
          father: "bg-5",
          children: "work-info",
          headline: "Project #5",
          paragraph: "Project Description",
        },
        {
          id: 86,
          parent: "work-6 rightToCenter",
          father: "bg-6",
          children: "work-info",
          headline: "Project #6",
          paragraph: "Project Description",
        },
        {
          id: 87,
          parent: "work-7 rightToCenter",
          father: "bg-7",
          children: "work-info",
          headline: "Project #7",
          paragraph: "Project Description",
        },
        {
          id: 88,
          parent: "work-8 rightToCenter",
          father: "bg-8",
          children: "work-info",
          headline: "Project #8",
          paragraph: "Project Description",
        },

        {
          id: 89,
          parent: "work-9 rightToCenter",
          father: "bg-9",
          children: "work-info",
          headline: "Project #9",
          paragraph: "Project Description",
        },
      ],
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
    },
    onShow() {
      if (this.show) return true;
      if (this.windowTop > 4320) {
        this.show = true;
        return true;
      }
      return false;
    },
  },
};
</script>

<style scoped>
.body-content8 {
  height: 60rem;
  text-align: center;
}

.body-content8 > .text-center h2 {
  padding-top: 12.5rem;
  letter-spacing: 5px;
  font-family: "Open Sans", sans-serif;
  font-size: 2rem;
  font-weight: 200;
  padding-bottom: 1rem;
}

.body-content8 > .text-center hr {
  width: 3rem;
  height: 3px;
  margin: 0 auto;
  background-color: rgb(173, 0, 255);
  border: none;
  margin-bottom: 2rem;
}

.body-content8 > .taskbar {
  padding-bottom: 1rem;
}

.body-content8 > .taskbar > ul {
  list-style: none;
}

.body-content8 > .taskbar > ul > li {
  display: inline-block;
  padding: 0 1rem;
}

.body-content8 > .taskbar > ul > li > a {
  text-decoration: none;
  color: var(--text-color);
}

.body-content8 > .taskbar > ul > li > a:hover {
  color: var(--primary-color);
}

.body-content8 > .taskbar > ul > li > a:focus {
  color: #56007f;
}

.body-content8 > .works {
  display: flex;
  margin: 0;
  padding: 0;
  flex-wrap: wrap;
}

.body-content8 > .works > .work-1 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-1 > .bg-1 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work1.jpg");
  background-size: cover;
}

.work-info {
  padding-top: 5rem;
  background-color: var(--primary-color);
  height: 100%;
  opacity: 0;
  cursor: pointer;
  color: white;
}

.work-info > p {
  padding-bottom: 5rem;
}

.body-content8 > .works > .work-1 > .bg-1:hover .work-info,
.body-content8 > .works > .work-1 > .bg-1:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-1 > .bg-1:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-2 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-2 > .bg-2 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work2.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-2 > .bg-2:hover .work-info,
.body-content8 > .works > .work-2 > .bg-2:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-2 > .bg-2:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-3 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-3 > .bg-3 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work3.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-3 > .bg-3:hover .work-info,
.body-content8 > .works > .work-3 > .bg-3:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-3 > .bg-3:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-4 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-4 > .bg-4 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work4.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-4 > .bg-4:hover .work-info,
.body-content8 > .works > .work-4 > .bg-4:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-4 > .bg-4:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-5 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-5 > .bg-5 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work5.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-5 > .bg-5:hover .work-info,
.body-content8 > .works > .work-5 > .bg-5:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-5 > .bg-5:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-6 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-6 > .bg-6 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work6.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-6 > .bg-6:hover .work-info,
.body-content8 > .works > .work-6 > .bg-6:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-6 > .bg-6:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-7 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-7 > .bg-7 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work7.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-7 > .bg-7:hover .work-info,
.body-content8 > .works > .work-7 > .bg-7:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-7 > .bg-7:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-8 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-8 > .bg-8 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work8.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-8 > .bg-8:hover .work-info,
.body-content8 > .works > .work-8 > .bg-8:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-8 > .bg-8:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-9 {
  width: 25%;
  overflow: hidden;
}

.body-content8 > .works > .work-9 > .bg-9 {
  width: 100%;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work1.jpg");
  background-size: cover;
}

.body-content8 > .works > .work-9 > .bg-9:hover .work-info,
.body-content8 > .works > .work-9 > .bg-9:focus .work-info {
  opacity: 0.8;
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .works > .work-9 > .bg-9:hover {
  transition: ease-in 1s;
  transform: scale(1.2);
}

.body-content8 > .bg-btn {
  background-color: var(--light-color);
  height: 10rem;
  padding-top: 3.5rem;
}

.body-content8 > .bg-btn > .btn {
  border-radius: 0;
  padding: 0.75rem 2rem;
  color: black;
  background-color: var(--light-color);
  border: 3px solid black;
  letter-spacing: 3px;
  font-size: 1rem;
}

.body-content8 > .bg-btn > .btn:hover {
  color: white;
  background-color: black;
}
</style>
