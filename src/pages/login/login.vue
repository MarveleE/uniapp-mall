<template>
  <view class="main">
    <view class="login-container">
      <text class="title">Welcom to Sexy Store</text>
      <view class="form-item">
        <input class="field" type="text" placeholder="请输入用户名" />
      </view>
      <view class="form-item">
        <input class="field" type="password" placeholder="请输入密码" />
      </view>
      <button class="login-button" :disabled="false" :loading="isLoading" open-type="" hover-class="button-hover"
        @click="buttonClick">
        登陆
      </button>
    </view>
  </view>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      'isLoading': false
    }
  },
  computed: {},
  methods: {
    buttonClick() {
      this.isLoading = !this.isLoading
      setTimeout(() => {
        this.isLoading = false
      }, 2000)
    }
  },
  watch: {},
}
</script>

<style>
.main {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100%;
  background-color: aqua;
}

.login-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 300px;
  background-color: #f5f5f5;
  width: 80%;
  border-radius: 10px;
}

.login-container>* {
  margin: 10px;
  width: 80%;
}

.form-item {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  padding: 10px;
  background-color: white;
  border-radius: 10px;
  height: 26px;
  align-items: center;
}

.field {
  width: 100%;
}

.title {
  justify-content: center;
  display: flex;
  font-size: 20px;
  color: black;
  font-weight: bolder;
}

.login-button {
  padding: 10px;
  height: 40px;
  justify-content: center;
  display: flex;
  align-items: center;
  border-radius: 10px;
  background-color: cadetblue;
  color: white;
  font-size: 20px;
  width: 90%;
}
</style>