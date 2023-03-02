<template>
  <div class="social-icons-container">
    <div class="social-icons">
      <a href="#">
        <i class="fab fa-facebook-f"></i>
      </a>
      <a href="#">
        <i class="fab fa-twitter"></i>
      </a>
      <a href="#">
        <i class="fab fa-instagram"></i>
      </a>
      <a href="#">
        <i class="fab fa-linkedin-in"></i>
      </a>
    </div>

    <div class="horizon-line mt-2"></div>
  </div>
</template>

<style>
.social-icons-container {
  position: fixed;
  bottom: 0;
  display: flex;
  flex-direction: column;
  left: 4%;
}

.horizon-line {
  width: 1px;
  height: 100px;
  background-color: #fff;
  opacity: 0.5;
  margin: 0 auto;
}

.social-icons {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: -15px;
}

.social-icons a {
  margin: 0 15px;
  color: #fff;
  font-size: 20px;
  transition: all 0.2s ease-in-out;
}

.social-icons a:hover {
  transform: scale(1.1);
}
</style>
