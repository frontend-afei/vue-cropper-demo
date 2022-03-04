<template>
  <div>
    <el-button @click="dialogVisible = true">上传头像</el-button>
    <avatar-cropper :dialogVisible.sync="dialogVisible" @closeAvatarDialog="closeAvatarDialog"></avatar-cropper>
  </div>
</template>

<script>
  import avatarCropper from '@/components/avatarCropper'
  export default {
    components: {
      avatarCropper
    },
    data() {
      return {
        dialogVisible: false
      }
    },
    methods: {
      closeAvatarDialog(data) {
        console.log(data)
        this.dialogVisible = false
      }
    }
  }
</script>
