<template>
  <div class="main-container">
    <div class="left-panel">
      </div>
    <div class="right-panel">
      <div class="login-card">
        <div class="logo">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-utensils">
            <path d="M3 2v7c0 1.1.9 2 2 2h4a2 2 0 0 0 2-2V2"/><path d="M7 15v6"/><path d="M12 21h4a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2H9v11a3 3 0 0 1-3 3H3"/><path d="M15 6h1a2 2 0 0 1 2 2v7a2 2 0 0 1-2 2h-1v-7a2 2 0 0 1 2-2z"/>
          </svg>
          <span>Hệ Thống Quản Lý Nhà Hàng</span>
        </div>
        <form @submit.prevent="handleLogin">
          <div class="form-group">
            <label for="username">Tài khoản</label>
            <input type="email" id="username" v-model="email" placeholder="lephucanh2004@gmail.com" required>
          </div>
          <div class="form-group">
            <label for="password">Mật khẩu</label>
            <input type="password" id="password" v-model="password" placeholder="Nhập mật khẩu" required>
          </div>
          <div class="forgot-password">
            <a href="#">Quên mật khẩu?</a>
          </div>
          <button type="submit" class="login-button">Đăng nhập</button>
        </form>
        <div class="signup-link">
          Chưa có tài khoản? <a href="#">Đăng kí</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginLayout',
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    handleLogin() {
      console.log('Logging in with:', this.email, this.password);
    }
  }
};
</script>

<style scoped>
.main-container {
  display: flex;
  height: 100vh;
  background-color: #f4f5f9;
  font-family: Arial, sans-serif;
}

.left-panel {
  flex: 1;
}

.right-panel {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.login-card {
  background: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  width: 380px;
  text-align: center;
}

.logo {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin-bottom: 25px;
  color: #333;
}

.logo svg {
  margin-right: 10px;
  width: 28px;
  height: 28px;
}

.logo span {
  font-weight: 600;
  font-size: 1.1rem;
}

.form-group {
  text-align: left;
  margin-bottom: 18px;
}

.form-group label {
  display: block;
  margin-bottom: 6px;
  font-weight: 500;
  color: #555;
}

.form-group input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 6px;
  box-sizing: border-box;
  font-size: 1rem;
}

.forgot-password {
  text-align: right;
  margin-bottom: 20px;
}

.forgot-password a {
  color: #007bff;
  text-decoration: none;
  font-size: 0.9rem;
}

.login-button {
  width: 100%;
  padding: 12px;
  border: none;
  background-color: #007bff;
  color: white;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: bold;
  transition: background-color 0.2s;
}

.login-button:hover {
  background-color: #0069d9;
}

.signup-link {
  margin-top: 20px;
  font-size: 0.9rem;
  color: #555;
}

.signup-link a {
  color: #007bff;
  text-decoration: none;
  font-weight: bold;
}
</style>
