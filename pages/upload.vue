<template>
  <div class="upload">
    <div class="h1 dark-blue">
      Upload
    </div>
    <div class="upload-url upload-section">
      <div class="h3">
        Video Link
      </div>
      <input type="text">
    </div>
    <div class="upload-file upload-section">
      <div class="h3">
        Upload File
      </div>
      <el-upload
        action="https://jsonplaceholder.typicode.com/posts/"
        list-type="picture-card"
        :on-preview="handlePictureCardPreview"
        :on-remove="handleRemove">
        <i class="el-icon-plus"></i>
      </el-upload>
      <el-dialog :visible.sync="dialogVisible">
        <img width="100%" :src="dialogImageUrl" alt="">
      </el-dialog>
    </div>
    <el-button type="primary">Submit</el-button>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
.upload {
  padding: 3em 3em;

  .h1 {
    margin-bottom: 2em;
  }

  .upload-section {
    margin-bottom: 3em;
    .h3 {
      margin-bottom: 0.6em;
    }
  }

  .upload-url {
    input {
      width: 300px;
      height: 2em;
      padding: 1em 0.5em;
      border: solid 1px $gray;
      font-size: 16px;
      border-radius: 5px;
    }
  }
}
</style>