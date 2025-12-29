# My-Personal-Website-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Personal Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(135deg, #667eea, #764ba2);
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
    }

    .container {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(15px);
      padding: 40px;
      border-radius: 20px;
      width: 100%;
      max-width: 400px;
      box-shadow: 0 25px 45px rgba(0,0,0,0.2);
      animation: fadeIn 1.2s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      text-align: center;
      margin-bottom: 10px;
      font-weight: 600;
    }

    p {
      text-align: center;
      font-size: 14px;
      margin-bottom: 30px;
      opacity: 0.9;
    }

    .input-group {
      margin-bottom: 20px;
    }

    label {
      font-size: 14px;
      display: block;
      margin-bottom: 6px;
    }

    input {
      width: 100%;
      padding: 12px;
      border-radius: 10px;
      border: none;
      outline: none;
      font-size: 14px;
    }

    input:focus {
      box-shadow: 0 0 0 2px #a78bfa;
    }

    button {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 12px;
      background: #8b5cf6;
      color: white;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #7c3aed;
      transform: translateY(-2px);
    }

    .footer-text {
      margin-top: 20px;
      text-align: center;
      font-size: 13px;
      opacity: 0.8;
    }

    .success {
      display: none;
      text-align: center;
      font-size: 18px;
      animation: fadeIn 1s ease;
    }

    .success span {
      font-size: 40px;
      display: block;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>

  <div class="container" id="loginBox">
    <h1>Welcome Back</h1>
    <p>Login to your personal website</p>

    <div class="input-group">
      <label>Username</label>
      <input type="text" id="username" placeholder="Enter your username">
    </div>

    <div class="input-group">
      <label>Password</label>
      <input type="password" id="password" placeholder="Enter your password">
    </div>

    <button onclick="login()">Login</button>

    <div class="footer-text">
      © 2025 • My Personal Website
    </div>
  </div>

  <div class="container success" id="successBox">
    <span>🎉</span>
    <h1>Hello!</h1>
    <p>You have successfully logged in.</p>
  </div>

  <script>
    function login() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      if (username && password) {
        document.getElementById("loginBox").style.display = "none";
        document.getElementById("successBox").style.display = "block";
      } else {
        alert("Please enter username and password");
      }
    }
  </script>

</body>
</html>
