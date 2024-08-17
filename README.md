<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
    <link rel="stylesheet" href="login.css">
</head>
<body>
    <div class="login-container">
        <h2>Login Form</h2>
        <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" required>
        </div>
        <div class="form-group">
            <label for="password">Password</label>
            <input type="password" id="password" required>
        </div>
        <button class="login-button" id="loginButton" disabled>Login</button>
    </div>

    <script>
        const emailInput = document.getElementById('email');
        const passwordInput = document.getElementById('password');
        const loginButton = document.getElementById('loginButton');

        emailInput.addEventListener('input', validateForm);
        passwordInput.addEventListener('input', validateForm);

        loginButton.addEventListener('mouseover', function() {
            if (loginButton.disabled) {
                const randomX = Math.floor(Math.random() * 300);
                const randomY = Math.floor(Math.random() * 300);
                loginButton.style.transform = `translate(${randomX}px, ${randomY}px)`;
            }
        });

        function validateForm() {
            if (emailInput.value && passwordInput.value) {
                loginButton.disabled = false;
                loginButton.style.transform = 'translate(0, 0)';
            } else {
                loginButton.disabled = true;
            }
        }
    </script>


   
</body>
</html>