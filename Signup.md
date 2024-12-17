 <link rel="icon" type="image/x-icon" href="https://icons.veryicon.com/png/o/miscellaneous/base-icon-library-1/internet-54.png"> 

<html><head><base href="." /><title>PeerChat Signup</title><style>
:root {
  --primary: #4a90e2;
  --secondary: #f5f7fa;
  --text: #2c3e50;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Inter', sans-serif;
  background: linear-gradient(135deg, var(--secondary) 0%, #ffffff 100%);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--text);
}

.signup-container {
  background: white;
  padding: 2.5rem;
  border-radius: 1rem;
  box-shadow: 0 10px 25px rgba(0,0,0,0.05);
  width: 100%;
  max-width: 400px;
  position: relative;
  overflow: hidden;
}

.logo {
  text-align: center;
  margin-bottom: 2rem;
}

.chat-icon {
  fill: var(--primary);
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0px); }
}

h1 {
  font-size: 1.5rem;
  text-align: center;
  margin-bottom: 1.5rem;
  color: var(--text);
}

.form-group {
  margin-bottom: 1.2rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
  font-weight: 500;
}

input {
  width: 100%;
  padding: 0.8rem;
  border: 2px solid #eee;
  border-radius: 0.5rem;
  font-size: 1rem;
  transition: all 0.3s;
}

input:focus {
  outline: none;
  border-color: var(--primary);
}

button {
  width: 100%;
  padding: 1rem;
  background: var(--primary);
  color: white;
  border: none;
  border-radius: 0.5rem;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

button:hover {
  background: #357abd;
  transform: translateY(-2px);
}

.alternative {
  text-align: center;
  margin-top: 1.5rem;
  font-size: 0.9rem;
}

.alternative a {
  color: var(--primary);
  text-decoration: none;
  font-weight: 500;
}

.alternative a:hover {
  text-decoration: underline;
}

.background-shapes {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: -1;
  opacity: 0.1;
}

</style></head><body>
  <div class="signup-container">
    <div class="logo">
      <svg class="chat-icon" width="48" height="48" viewBox="0 0 24 24">
        <path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm0 14H6l-2 2V4h16v12z"/>
        <path d="M7 9h2v2H7zm4 0h2v2h-2zm4 0h2v2h-2z"/>
      </svg>
    </div>
    
    <h1>Join PeerChat Today</h1>
    
    <form id="signupForm">
      <div class="form-group">
        <label for="username">Username</label>
        <input type="text" id="username" required placeholder="Choose a username">
      </div>
      
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" required placeholder="Enter your email">
      </div>
      
      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" required placeholder="Create a password">
      </div>
      
      <div class="form-group">
        <label for="confirmPassword">Confirm Password</label>
        <input type="password" id="confirmPassword" required placeholder="Confirm your password">
      </div>
      
      <button type="submit">Create Account</button>
    </form>
    
    <div class="alternative">
      Already have an account? <a href="https://peerchat.com/login">Log in</a>
    </div>

    <svg class="background-shapes" width="100%" height="100%">
      <defs>
        <pattern id="pattern" x="0" y="0" width="40" height="40" patternUnits="userSpaceOnUse">
          <circle cx="20" cy="20" r="2" fill="var(--primary)"/>
        </pattern>
      </defs>
      <rect width="100%" height="100%" fill="url(#pattern)"/>
    </svg>
  </div>

  <script>
    document.getElementById('signupForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      const username = document.getElementById('username').value;
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;
      const confirmPassword = document.getElementById('confirmPassword').value;
      
      // Basic validation
      if (password !== confirmPassword) {
        alert('Passwords do not match!');
        return;
      }
      
      if (password.length < 8) {
        alert('Password must be at least 8 characters long!');
        return;
      }
      
      // Here you would typically make an API call to your backend
      console.log('Form submitted:', {
        username,
        email,
        password
      });
      
      // Show success message
      alert('Account created successfully! Please check your email to verify your account.');
      
      // Reset form
      this.reset();
    });
    
    // Add floating animation to inputs on focus
    const inputs = document.querySelectorAll('input');
    inputs.forEach(input => {
      input.addEventListener('focus', function() {
        this.parentElement.style.transform = 'translateY(-2px)';
      });
      
      input.addEventListener('blur', function() {
        this.parentElement.style.transform = 'translateY(0)';
      });
    });
  </script>
</body></html>
