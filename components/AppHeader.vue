<template>
  <div class="container1">
    <SocialMedia />
    <section class="app__header">
      <div class="app__header-bg" />
      <div class="app__header-content">
        <div class="sub_title">
          <div />
          <p>A Hiking guide</p>
        </div>
        <h1 class="title">Be prepared for the Mountains and beyond!</h1>
        <div class="action">
          <p>scroll down</p>
          <img src="../assets/images/arrow_downward.svg" alt="arrow icon" />
        </div>
      </div>
    </section>
    <AppNavigation :active="'Start'" />
  </div>
</template>

<script>
import SocialMedia from "./SocialMedia.vue";
import AppNavigation from "./AppNavigation.vue";

export default {
  components: { SocialMedia, AppNavigation },
  name: "AppHeader",
};
</script>

<style>
.container1 {
  display: flex;
  justify-content: space-between;
  height: 120vh;
}

.transition-group {
  position: absolute;
  bottom: 0;
  left: 0px;
  width: 100%;
  height: 200px;
  background: linear-gradient(
    180deg,
    rgba(11, 29, 38, 0) 0%,
    rgba(11, 29, 38, 0.5) 50%,
    rgba(11, 29, 38, 1) 100%
  );
  border: 1px solid red;
  z-index: 100;
}

.app__header {
  height: auto;
  width: 100%;
  z-index: 1;
  left: 0;
  top: -130px;
  position: relative;
}

.app__header-bg {
  background: linear-gradient(
      to bottom,
      rgba(11, 29, 38, 0) 0%,
      rgba(11, 29, 38, 0.5) 80%,
      rgba(11, 29, 38, 1) 100%
    ),
    url("../assets/images/bg-image.webp") no-repeat;
  background-size: cover;

  height: 100%;
}

.app__header-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  width: 70%;
  height: auto;
  left: 50%;
  top: 50%;
  justify-content: center;
  transform: translate(-50%, -50%);
  position: absolute;
}

.app__header-content .sub_title {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  width: 100%;

  margin-bottom: 32px;
}

.app__header-content .sub_title div {
  width: 72px;
  border: 2px solid var(--color-accent);
  background: var(--color-accent);
  margin-right: 32px;
}

.app__header-content .sub_title p {
  font-family: var(--font-base);
  font-weight: 900;
  font-size: 18px;
  line-height: 21px;
  letter-spacing: 6px;
  text-transform: uppercase;
  color: var(--color-accent);
}

.app__header-content .title {
  font-family: var(--font-base);
  font-weight: 900;
  font-size: 88px;
  line-height: 100px;
  text-transform: capitalize;
  color: var(--color-white);
  margin-bottom: 32px;
}

.app__header-content .action {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  cursor: pointer;
}

.app__header-content .action:hover {
  border-bottom: 2px solid var(--color-accent);
}

.app__header-content .action p {
  font-family: var(--font-base);
  font-weight: 700;
  font-size: 18px;
  line-height: 21px;
  color: var(--color-white);

  margin-right: 20px;
}

.app__header-content .action img {
  width: 16px;
  height: 24px;
}

@media screen and (min-width: 1700px) {
  .container1 {
    height: 190vh;
  }

  .app__header-content {
    top: 30%;
  }

  .app__header-bg {
    height: 100%;
  }
}

@media screen and (max-width: 1024px) {
  .app__header-content {
    align-items: center;
    text-align: center;
  }

  .app__header-content .sub_title {
    justify-content: center;
    margin-bottom: 10px;
  }

  .app__header-content .sub_title div {
    width: 48px;
    border: 2px solid var(--color-accent);
    background: var(--color-accent);
    margin-right: 32px;
  }

  .app__header-content .title {
    font-size: 48px;
    line-height: 60px;
  }
}

@media screen and (max-width: 786px) {
  .app__header-content {
    top: 40%;
  }

  .app__header-content .title {
    font-size: 36px;
    line-height: 60px;
  }
}

@media screen and (max-width: 500px) {
  .app__header-content .app__header-bg {
    height: 260vh;
  }
}
</style>
