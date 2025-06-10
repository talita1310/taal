<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Register - iqbal hafis Media Sosial</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }
    body {
      background: linear-gradient(to right, #74ebd5, #ACB6E5);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background-color: white;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      max-width: 400px;
      width: 100%;
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }
    label {
      display: block;
      margin-bottom: 5px;
      font-weight: 600;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 14px;
    }
    button {
      width: 100%;
      padding: 12px;
      background-color: #007bff;
      border: none;
      border-radius: 8px;
      color: white;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Registrasi Web iqbal</h2>
    <form onsubmit="return registerUser()">
      <label for="Username">Username:</label>
      <input type="text" id="username" required>

      <label for="password">Password:</label>
      <input type="password" id="password" required>

      <label for="confirm-password">Konfirmasi Password:</label>
      <input type="password" id="confirm-password" required>

      <button type="submit">Register</button>
    </form>
  </div>

  <script>
    function registerUser() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const confirmPassword = document.getElementById("confirm-password").value;

      if (password !== confirmPassword) {
        alert("Password dan konfirmasi password tidak cocok!");
        return false;
      }

      localStorage.setItem("username", username);
      window.location.href = "ye.html";
      return false;
    }
  </script>
</body>
</html>
