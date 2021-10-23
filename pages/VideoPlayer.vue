<template>
  <div class="video-player">
    <div class="h1 dark-blue">
      Video Player
    </div>
    <div class="play-list">
      <div class="image"></div>
      <div class="image"></div>
      <div class="image"></div>
    </div>
    <div class="display">
      <iframe class="video" src="https://www.youtube.com/embed/JQkuncaEcnI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      <div class="subtitle-area">
        <input type="text">
        <div class="subtitle regular white"></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
.video-player {
  padding: 3em 0 0 3em;

  .h1 {
    margin-bottom: 2em;
  }

  .play-list {
    display: flex;
    flex-wrap: nowrap;
    margin-bottom: 3em;

    .image {
      width: calc(1280px * 0.15);
      height: calc(720px * 0.15);
      background-color: $dark-blue;
      margin-right: 1em;
    }
  }

  .display {
    display: flex;
    flex-wrap: nowrap;
    margin-bottom: 3em;

    .video {
      width: calc(1280px * 0.55);
      height: calc(720px * 0.55);
      background-color: $gray;
      margin-right: 3em;
    }

    .subtitle-area {
      background-color: $dark-blue;
      padding: 2em 2em;

      input {
        width: 200px;
        height: 1em;
        padding: 1em 0.5em;
        border: solid 1px $gray;
        font-size: 16px;
        border-radius: 5px;
      }
    }
  }
}
</style>