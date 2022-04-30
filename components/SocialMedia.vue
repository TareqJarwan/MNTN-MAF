<template>
  <div class="app__social">
    <p>FOLLOW US</p>
    <a href="https://www.instagram.com/" target="_blank">
      <img src="../assets/images/instgram-icon.svg" alt="instgram" />
    </a>
    <a href="https://www.twitter.com" target="_blank">
      <img src="../assets/images/twitter-icon.svg" alt="twitter" />
    </a>
  </div>
</template>

<script>
export default {
  name: "SocialMedia",
};
</script>

<style>
.app__social {
  width: 90px;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
  height: 100%;
  margin: 2rem 0;
  align-items: center;
  z-index: 10000;
}

.app__social p {
  font-family: "Roboto";
  font-style: normal;
  width: 100%;
  font-weight: 700;
  font-size: 18px;
  line-height: 21px;
  color: #ffffff;
  transform: rotate(90deg);
  transition: all 0.3s ease-in-out;
  white-space: nowrap;
}

.app__social img {
  width: 20px;
  height: 20px;
  cursor: pointer;
  margin-bottom: 1.5rem;
  transition: all 0.3s ease-in-out;
}

.app__social a:first-of-type {
  margin-top: 5rem;
}

@media screen and (min-width: 2000px) {
  .app__social {
    width: 120px;
  }
  .app__social p {
    font-size: 24px;
    line-height: 24px;
  }

  .app__social img {
    width: 50px;
    height: 50px;
  }

  .app__social a:first-of-type {
    margin-top: 10rem;
  }
}

@media screen and (max-width: 650px) {
  .app__social {
    display: none;
  }
}
</style>
