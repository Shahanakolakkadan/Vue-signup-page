<script>
  export default {
    data() {
      return {
        username: '',
        email: '',
        password: '',
      };
    },
    methods: {
      submitForm() {
        // Perform signup logic here (e.g., send data to the server)
        console.log('Form submitted:', { username: this.username, email: this.email, password: this.password });

        // You can make an API call to your server to handle user registration
        // For simplicity, we're just logging the form data in the console
      },
    },
  };
</script>

<template>
    <div class="form-content">
      <div class="form-header">
        <h2>Sign Up</h2>
      </div>
      <div class="form-body d-flex flex-column">
        <form @submit.prevent="submitForm">
          <div class="form-name">
            <label for="username">Username: </label><br>
            <input type="text" id="username" v-model="username" required /><br>
          </div>
          
          <div class="form-mail">
            <label for="email">Email: </label><br>
            <input type="email" id="email" v-model="email" required /><br>
          </div>
          
          <div class="form-password">
            <label for="password">Password: </label><br>
            <input type="password" id="password" v-model="password" required /><br>
          </div>
          <div class="form-button">
            <button type="submit">Sign Up</button>
          </div>
        </form>
      </div>
    </div>
</template>
  
<style scoped>
  /* Add your component-specific styles here */
  .form-content {
    display: flex;
    flex-direction: column;
    place-content: center;
    align-items: center;
  }
  .form-header {
    font-size: 28px;
    font-weight: 500;
    color: black;
  }
  .form-body {
    background-color: grey;
    font-size: 20px;
    padding: 50px;
  }
  .form-body input {
      width: 400px; 
      height: 40px;
      margin-top: 10px;
      margin-bottom: 10px;
  }
  .form-button {
    margin-top: 30px;
    text-align: center;
  }
  .form-button button {
    background-color: black; 
    color: white;
    width: 250px;
    height: 50px;
  }
</style>
  