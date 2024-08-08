<template>
  <div class="logo">
    <div class="bird"></div>
  </div>
</template>

<script setup>
// 不需要特別的 JavaScript 代碼
</script>

<style scoped>
.logo {
  width: 3rem;
  aspect-ratio: 1;
  border-radius: 50%;
  box-shadow: 0px 0px 5px 1px rgba(0, 0, 0, 0.25);
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: white;
  z-index: 10;
}

.bird {
  width: 50%;
  height: 50%;
  border-bottom: 5px solid rgba(0, 0, 0, 0.8);
  border-top: 5px solid rgba(0, 0, 0, 0.8);
  border-radius: 80% 40% 45% 0;
  position: relative;
}

.bird::after {
  content: '';
  width: 5px;
  aspect-ratio: 1;
  border-radius: 50%;
  background-color: rgba(0, 0, 0, 0.8);
  position: absolute;
  top: 50%;
  right: 20%;
  transform: translateY(-50%);
}

.bird::before {
  content: '';
  width: 7.5px;
  aspect-ratio: 5/3;
  border-radius: 0 100% 0 0;
  background-color: rgba(0, 0, 0, 0.8);
  transform: rotate(-10deg);
  position: absolute;
  top: 25%;
  right: -7.5px;
}

/* RWD */
@media (min-width: 1280px) {
  .logo {
    position: absolute;
    top: 3rem;
    right: 0;
    transform: translate(50%, 0);
    width: 6rem;
  }

  .bird {
    width: 55%;
    height: 50%;
    border-bottom: 10px solid rgba(0, 0, 0, 0.8);
    border-top: 10px solid rgba(0, 0, 0, 0.8);
    border-radius: 80% 40% 45% 0;
  }

  .bird::after {
    width: 10px;
  }

  .bird::before {
    width: 15px;
    right: -15px;
  }
}
</style>
