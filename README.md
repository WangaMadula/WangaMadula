<!DOCTYPE html>
<html lang="en">
<head >
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login and Registration Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="wrapper">
        <div class="form-wrapper login">
            <form action="" id="login-form">
                <h2>Login</h2>
                <div class="input-box">
                    <span class="icon"></span>
                    <input type="email" placeholder="Email" required id="email">
                </div>
                <div class="input-box">
                    <span class="icon"></span>
                    <input type="password" placeholder="Password" required id="password">
                </div>
                <div class="forgot-pass">
                    <a href="#">Forgot Password</a>
                </div>
                <button type="submit">Login</button>
                <div class="sign-link">
                    <p>Don't have an account? <a href="#" id="register-link">Register</a></p>
                </div>
            </form>
        </div>
        <div class="form-wrapper register">
            <form action="" id="register-form">
                <h2>Register</h2>
                <div class="input-box">
                    <span class="icon"></span>
                    <input type="email" placeholder="Email" required id="register-email">
                </div>
                <div class="input-box">
                    <span class="icon"></span>
                    <input type="password" placeholder="Password" required id="register-password">
                </div>
                <div class="input-box">
                    <span class="icon"></span>
                    <input type="password" placeholder="Confirm Password" required id="register-confirm-password">
                </div>
                <button type="submit">Register</button>
            </form>
        </div>
    </div>

    <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
    <script src="script.js"></script>
</body>
</html>

body {
    margin: 0;
    color: #6a6f8c;
    background: #7A288A;
    font: 600 16px/18px "Open Sans", sans-serif;
}

.wrapper {
    width: 100%;
    height:  100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.form-wrapper {
    width: 300px;
    background: transparent;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border: 2px solid #4CAF50;
    backdrop-filter: blur(10px);
}

.form-wrapper.login {
    display: block;
}

.form-wrapper.register {
    display: none;
}

.input-box {
    margin-bottom: 20px;
}

.input-box span.icon {
    position: absolute;
    left: 10px;
    top: 10px;
    font-size: 18px;
    color: #4CAF50;
}

.input-box input[type="email"],
.input-box input[type="password"] {
    width: 250px;
    height: 30px;
    padding: 10px;
    border: none;
    border-radius: 10px;
    font-size: 16px;
    background: rgba(255, 255, 255, 0.2);
    color: #fff;
}

.forgot-pass {
    margin-bottom: 20px;
}

.forgot-pass a {
    color: #4CAF50;
    text-decoration: none;
}

.sign-link {
    margin-top: 20px;
}

.sign-link p {
    margin-bottom: 10px;
}

.sign-link a {
    color: #4CAF50;
    text-decoration: none;
}

button[type="submit"] {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 10px;
    background: #4CAF50;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
}

button[type="submit"]:hover {
    background: #3e8e41;
}

<?php
const loginForm = document.getElementById('login-form');
const registerForm = document.getElementById('register-form');
const registerLink = document.getElementById('register-link');

registerLink.addEventListener('click', () => {
    document.querySelector('.form-wrapper.login').style.display = 'none';
    document.querySelector('.form-wrapper.register').style.display = 'block';
});

loginForm.addEventListener('submit', (e) => {
    e.preventDefault();
    // Add login functionality here
});

registerForm.addEventListener('submit', (e) => {
    e.preventDefault();
    // Add register functionality here
});
?>
