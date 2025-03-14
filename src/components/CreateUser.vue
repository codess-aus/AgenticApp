<template>
  <div class="create-user">
    <h2>Create a New User</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="firstName">First Name:</label>
        <input 
          type="text" 
          id="firstName" 
          v-model="user.firstName" 
          required
        />
      </div>
      
      <div class="form-group">
        <label for="lastName">Last Name:</label>
        <input 
          type="text" 
          id="lastName" 
          v-model="user.lastName" 
          required
        />
      </div>
      
      <div class="form-group">
        <label for="email">Email:</label>
        <input 
          type="email" 
          id="email" 
          v-model="user.email" 
          required
        />
      </div>
      
      <div class="form-group">
        <label for="password">Password:</label>
        <input 
          type="password" 
          id="password" 
          v-model="user.password" 
          required
          minlength="8"
        />
      </div>
      
      <button type="submit" class="submit-btn">Create User</button>
    </form>
    
    <div v-if="message" class="message" :class="{ success: isSuccess }">
      {{ message }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'CreateUser',
  data() {
    return {
      user: {
        firstName: '',
        lastName: '',
        email: '',
        password: ''
      },
      message: '',
      isSuccess: false
    }
  },
  methods: {
    submitForm() {
      // In a real app, this would connect to an API
      console.log('User submitted:', this.user);
      
      // Simulate a successful API call
      this.message = `User ${this.user.firstName} ${this.user.lastName} created successfully!`;
      this.isSuccess = true;
      
      // Reset the form
      this.user = {
        firstName: '',
        lastName: '',
        email: '',
        password: ''
      };
    }
  }
}
</script>

<style scoped>
.create-user {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 16px;
}

.submit-btn {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 12px 20px;
  font-size: 16px;
  border-radius: 4px;
  cursor: pointer;
  margin-top: 10px;
  width: 100%;
}

.submit-btn:hover {
  background-color: #3aa876;
}

.message {
  margin-top: 20px;
  padding: 10px;
  border-radius: 4px;
  text-align: center;
}

.success {
  background-color: #d4edda;
  color: #155724;
  border: 1px solid #c3e6cb;
}
</style>