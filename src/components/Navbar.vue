<template>
  <div class="container-fluid">
    <nav class="navbar navbar-dark bg-success">
      <div class="container-fluid">
        <img
          src="https://brand.tcu.edu/wp-content/uploads/2015/12/TCULogo_purple_5X7-01.jpg"
          class="float-start"
          alt="..."
          style="width: 90px"
        />

        <div
          class="nav-link nav-link-custom-2 d-flex flex-row justify-content-end align-items-center bg-light mx-5"
        >
          <!-- <router-link to="/teacher/dashboard">Dashboard</router-link> -->
          <div v-for="(section,index) in sections" :key="index" class="mx-4">
            <router-link :to="'/' + section.id">{{ section.id }} . {{ section.section }}</router-link>
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
      sections: [
        { id: "01", section: "About" },
        { id: "02", section: "Experiences" },
        { id: "03", section: "Project" },
        { id: "04", section: "Contact" }
      ]
    };
  }
};
</script>

<style>
.navbar {
  width: 100%;
  color: #fff;
  background-color: transparent;
  position: fixed;
  top: 0;
}
.nav-link-custom-2 {
  font-size: 0.95rem;
  font-family: "Rubik", serif;
}
</style>