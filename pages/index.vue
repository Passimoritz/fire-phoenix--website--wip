<template>
  <div class="main">
    <b-button class="btn-floating" to="/team">
      <b-icon icon="arrow-left" />
      Zum Team
    </b-button>
    <img class="image" src="../assets/images/phoenix.png">
    <video class="video" src="../assets/videos/main.mp4" autoplay loop muted />
  </div>
</template>

<script>
export default {
  head: {
    title: 'Startseite'
  }
}
</script>

<style lang="scss">
body {
  overflow: hidden;
}
.main {
  text-align: center;
}

.btn-floating {
  background: $color-primary;
  position: relative;
  z-index: 1000;
  transition: .33s;

  & > * {
    transition: .33s;
  }

  &:hover {
    background-color: rgba($color-primary, .8);

    & > * {
      transform: rotate(180deg);
      margin-right: 11px;
    }

  }
}

.video {
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  transition: 3.4s;
  z-index: 0;
}

.image {
  z-index: 1;
  position: absolute;
  left: 0;
  right: 0;
  margin: 0 auto;
  margin-top: 40px;
  width: 40%;
  transition: 1.4s;

  &:hover {
    opacity: 0;

    &+ .video {
      opacity: 1;
    }
  }
}

</style>
