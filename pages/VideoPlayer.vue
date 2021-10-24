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
    
    <el-button class="snap-shot-btn" type="primary" icon="el-icon-camera" @click="open">Snap shot</el-button>
    <div class="display">
      <iframe id="player" class="video" src="https://www.youtube.com/embed/JQkuncaEcnI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      <div class="subtitle-area">
        <div class="input-section">
          <input type="text" @keyup.enter="jumpTo()">
        </div>
        <div class="subtitle regular white">
          <div v-for="subtitle in raw.split('\n' + '' + '\n')" :key='subtitle' class="subtitle-block">
            {{ subtitle.split('\n')[2] }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import raw from '~/assets/str/Week 1 Tutorial.srt';

  export default {
    data() {
      return {
        raw,
        caption: [],
        alert: false
      }
    },
    methods: {
      jumpTo() {
        document.querySelector('.video').start = 318;
      },
      
      open() {
        this.$message({
          message: 'Snap Shot has been sent',
          type: 'success'
        });
      },

      openVn() {
        const h = this.$createElement;
        this.$message({
          message: h('p', null, [
            h('span', null, 'Message can be '),
            h('i', { style: 'color: teal' }, 'VNode')
          ])
        });
      }
    
    },
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

  .snap-shot-btn {
    margin-bottom: 1em;
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

      .input-section {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: .8em .8em;
        input {
          height: 1em;
          padding: 1em 0.5em;
          border: solid 1px $gray;
          font-size: 16px;
          border-radius: 5px;
          width: 100%;
        }
      }

      .subtitle {
        height: calc(720px * 0.55 - 60px);
        overflow: auto;
        padding: 0 1em;
      }

      .subtitle-block {
        padding: .8em .5em;
        border-bottom: solid $white 0.1px;
      }
    }
  }
}
</style>