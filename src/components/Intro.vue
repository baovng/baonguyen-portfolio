<template>
  <div class="container vh-100 heading-wrapper">
    <div class="d-flex align-items-start flex-column justify-content-center mx-5 vh-100">
      <h6 class="big-heading bh1 mb-3">{{ h1 }}</h6>
      <h1 class="big-heading bh2">{{ h2 }}</h1>
      <h1 class="big-heading bh2">{{ h3 }}</h1>
      <h6 class="mt-3 big-heading bh3 bh4">
        I'm in my last year studying computer information technology and web developer at
        <span
          style="color: var(--primary-color)"
        >Texas Christian University</span> . I'm currently
        looking for a full-time job before I graduate in 2023!
      </h6>
      <button class="btn btn-lg btn-custom mt-4 px-4 text-uppercase">See my Resume</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      h1: "Hi, my name is",
      h2: "Bao Nguyen.",
      h3: "I build things for website."
    };
  }
};
</script>

<style>
.heading-wrapper {
  width: 100%;
  max-width: 1080px;
}
.big-heading {
  font-family: "Be Vietnam Pro", serif;
  text-align: left;
}
.bh1 {
  color: var(--primary-color);
}
.bh2 {
  font-size: 4rem;
  line-height: 5rem;
  font-weight: 900;
}
.bh3 {
  font-family: "Roboto", serif;
  line-height: 2rem;
  font-size: 1rem;
}
.bh4 {
  width: 60%;
}
.btn-custom {
  border-radius: 0;
  font-size: 1rem;
  color: var(--primary-color);
  border-color: var(--primary-color);
}
.btn-custom:hover {
  background-color: var(--background-color);
  color: var(--primary-color);
}

.btn:focus {
  box-shadow: none;
}
</style>
