<template>
  <div id="navbar">
    <div class="nav-brand">
      <img src="" alt="">
      <div class="h2 gray">E-Learning tool</div>
    </div>
    <ul class="nav-item-list">
      <nuxt-link to="/">
        <li class="nav-item h3 gray">
          <i class="el-icon-s-home"></i>
          Overview
        </li>
      </nuxt-link>
      <nuxt-link to="/VideoPlayer">
        <li class="nav-item h3 gray">
          <i class="el-icon-video-play"></i>
          Video Player
        </li>
      </nuxt-link>
      <nuxt-link to="/Upload">
        <li class="nav-item h3 gray">  
          <i class="el-icon-upload"></i>
          Upload
        </li>
      </nuxt-link>
    </ul>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
#navbar {
  background-color: $dark-blue;
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 255px;
  // padding: 10px 20px;
}

.nav-brand {
  text-align: center;
  h1 {
    color: $light-blue;
  }
}

ul {
  list-style-type: none;
  padding: 0;

  a {
    color: $light-blue;
    text-decoration: none;

    li {
      // list-style-type: none;
      transition: 0.5s;
      padding: 1em 0 1em 32px;
      &:hover {
        background-color: #9FA2B4;
        color: $dark-blue;
      }

      i {
        margin-right: 24px;
      }
    }
  }
}

</style>