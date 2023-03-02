<template>
  <div>
    <svg viewBox="0 0 100 104" class="hexagon" :class="{ 'fade-out': isFadedOut }">
      <polygon
        points="50,3 94,28 94,77 50,102 8,77 8,28"
        fill="transparent"
        stroke="#fff"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="5"
      />
    </svg>
    <div class="letter-b-container">
      <div class="letter-b" v-if="isDrawn" :class="{ 'fade-out': isFadedOut }">B</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDrawn: false,
      isFadedOut: false
    };
  },
  mounted() {
    setTimeout(() => {
      this.isDrawn = true;
    }, 1000);
    setTimeout(() => {
      this.isFadedOut = true;
    }, 2500);
  }
};
</script>

<style>
.hexagon {
  display: flex;
  stroke-dasharray: 350;
  stroke-dashoffset: 350;
  stroke-linecap: butt;
  animation: draw-hexagon 1.1s ease-in-out forwards 0.2s;
}

.letter-b-container {
  position: relative;
  width: 100px;
  height: 104px;
  top: 50%;
  left: 50%;
  transform: translate(-48%, -96%);
  font-size: 50px;
  line-height: 100px;
  text-align: center;
}

.letter-b {
  position: absolute;
  font-family: "Roboto", sans-serif;
  font-weight: bold;
  font-size: 1.2em;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  animation: fade-in 0.5s ease-in-out forwards 0.3s;
}

@keyframes draw-hexagon {
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade-out {
  from {
    opacity: 1;
    transform: scale(1);
  }
  to {
    opacity: 0;
    transform: scale(0);
  }
}

.hexagon.fade-out {
  animation: fade-out 0.5s ease-in-out forwards;
}

.letter-b.fade-out {
  animation: fade-out 0.2s ease-in-out forwards;
}
</style>
