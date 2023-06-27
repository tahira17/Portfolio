<template>
  <header>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
    />
    <nav class="topnav" :class="{ responsive: isResponsive }" ref="topnav">
      <a href="javascript:void(0);" class="icon" @click="toggleMenu">
        <i class="fa fa-bars"></i>
      </a>
      <ul class="flex justify-center">
        <li>
          <RouterLink to="/"></RouterLink>
          <RouterLink
            to="/"
            class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white"
          >Home</RouterLink>
          <RouterLink
            to="/about"
            class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white"
          >About</RouterLink>
          <RouterLink
            to="/gitproject"
            class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white"
          >Git Projects</RouterLink>
          <RouterLink
            to="/liveproject"
            class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white"
          >Live Projects</RouterLink>
          <RouterLink
            to="/resume"
            class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white"
          >Resume</RouterLink>
        </li>
      </ul>
    </nav>
    <div>
      <hr class="border-1 my-8 border-gray-400 sm:w-4/12 mx-auto" />
    </div>
  </header>
</template>
  
  <script>
export default {
  data() {
    return {
      isResponsive: false
    };
  },
  methods: {
    toggleMenu() {
      this.isResponsive = !this.isResponsive;
    }
  }
};
</script>
  
  <style scoped>
.icon {
  background: #8dbdfffa !important;
}
.topnav {
  overflow: hidden;
}

.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color: blue;
  color: white;
}

.topnav a.active {
  background-color: blue;
  color: white;
}

.topnav .icon {
  display: none;
}

@media screen and (max-width: 600px) {
  .topnav a:not(:first-child) {
    display: none;
  }

  .topnav a.icon {
    float: right;
    display: block;
  }

  .topnav.responsive .icon {
    position: absolute;
    top: 0;
    right: 0;
  }

  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
}
</style>
  