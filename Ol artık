<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Giriş & Kayıt Formu</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #2c2c2c, #4f4f4f);
      background-image: url("https://www.transparenttextures.com/patterns/dark-mosaic.png");
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background-color: #1e1e1e;
      padding: 30px 25px;
      border-radius: 12px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.6);
      width: 350px;
      max-width: 90%;
      color: #f0f0f0;
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    form {
      display: none;
      flex-direction: column;
    }
    form.active {
      display: flex;
    }
    input {
      padding: 12px;
      margin: 10px 0;
      border: none;
      border-radius: 6px;
      background-color: #333;
      color: #fff;
      font-size: 1em;
    }
    input::placeholder {
      color: #aaa;
    }
    button {
      padding: 12px;
      background-color: #e0e0e0;
      color: #111;
      font-weight: bold;
      border: none;
      border-radius: 6px;
      font-size: 1em;
      cursor: pointer;
      transition: background-color 0.3s ease;
      margin-top: 10px;
    }
    button:hover {
      background-color: #ffffff;
    }
    .switch {
      margin-top: 15px;
      text-align: center;
      font-size: 0.9em;
    }
    .switch a {
      color: #f1f1f1;
      text-decoration: underline;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2 id="form-title">Giriş Yap</h2>

    <!-- Login Form -->
    <form id="login-form" class="active">
      <input type="email" placeholder="E-posta" required />
      <input type="password" placeholder="Şifre" required />
      <button type="submit">Giriş Yap</button>
    </form>

    <!-- Signup Form -->
    <form id="signup-form">
      <input type="text" placeholder="Kullanıcı Adı" required />
      <input type="email" placeholder="E-posta" required />
      <input type="password" placeholder="Şifre" required />
      <button type="submit">Kayıt Ol</button>
    </form>

    <div class="switch">
      <span id="switch-text">Hesabın yok mu? <a id="toggle">Kayıt Ol</a></span>
    </div>
  </div>

  <script>
    const loginForm = document.getElementById("login-form");
    const signupForm = document.getElementById("signup-form");
    const toggle = document.getElementById("toggle");
    const title = document.getElementById("form-title");
    const switchText = document.getElementById("switch-text");

    toggle.addEventListener("click", () => {
      const isLogin = loginForm.classList.contains("active");

      if (isLogin) {
        loginForm.classList.remove("active");
        signupForm.classList.add("active");
        title.textContent = "Kayıt Ol";
        switchText.innerHTML = 'Zaten hesabın var mı? <a id="toggle">Giriş Yap</a>';
      } else {
        signupForm.classList.remove("active");
        loginForm.classList.add("active");
        title.textContent = "Giriş Yap";
        switchText.innerHTML = 'Hesabın yok mu? <a id="toggle">Kayıt Ol</a>';
      }

      // Toggle’a yeniden event bağla
      document.getElementById("toggle").addEventListener("click", arguments.callee);
    });
  </script>
</body>
</html>
