<template>
  <div class="container-fluid ps-0 bg-light">
    <nav class="navbar" :class="navbarClasses" :style="{'transform': translateY}">
      <div class="container-fluid">
        <img src="@/assets/logo.png" class="float-start m-3 ms-5" alt="..." style="width: 45px" />

        <div
          class="nav-link nav-link-custom-2 d-flex flex-row justify-content-end align-items-center"
        >
          <!-- <router-link to="/teacher/dashboard">Dashboard</router-link> -->
          <div v-for="(section,index) in sections" :key="index" class="mx-4">
            <router-link :to="'/' + section.id" class="nav-text-custom">
              <span>{{ section.id }} .</span>
              {{ section.section }}
            </router-link>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHidden: false,
      isFixed: false,
      prevScrollPosition: window.pageYOffset,
      sections: [
        { id: "01", section: "About" },
        { id: "02", section: "Experiences" },
        { id: "03", section: "Project" },
        { id: "04", section: "Contact" }
      ]
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      const currentPosition = window.pageYOffset;

      const scrollDirection =
        currentPosition > this.prevScrollPosition ? "down" : "up";

      if (scrollDirection === "down") {
        //scroll down, hide navbar after delay
        this.isHidden = true;
        this.isFixed = false;
      } else {
        //scroll up, show navbar
        this.isHidden = false;
        if (currentPosition < window.innerHeight * 0.2) {
          this.isFixed = false;
        } else {
          this.isFixed = true;
        }
      }
      this.prevScrollPosition = currentPosition;
    }
  },
  computed: {
    navbarClasses() {
      return {
        "navbar-hidden": this.isHidden,
        "box-shadow": this.isFixed && !this.isHidden
      };
    },
    translateY() {
      return `translateY(${this.isHidden ? "-100%" : 0})`;
    }
  }
};
</script>

<style>
.navbar {
  width: 100%;
  background: none;
  background-color: rgba(30, 30, 30);
  position: fixed;
  top: 0;
  backdrop-filter: blur(8px);
  border: none;
  transition: transform 0.38s ease-in-out;
  z-index: 10;
  box-shadow: none;
}

.navbar-hidden {
  transform: translateY(-100%);
  box-shadow: none;
}
.box-shadow {
  box-shadow: 0 2px 10px rgba(20, 20, 20, 0.8);
  background-color: rgba(30, 30, 30, 0.1);
}
.nav-link-custom-2 {
  font-size: 0.95rem;
  font-family: "Rubik", serif;
}
.nav-text-custom {
  color: var(--text-color1);
  text-decoration: none;
}
.nav-text-custom:hover {
  color: var(--primary-color);
}
.nav-text-custom > span {
  color: var(--primary-color);
}
</style>