<!DOCTYPE html>
<html>
<head>
    <title>Login</title>

    <!-- Material Icons -->
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

    <style>

        /* FIX: prevents overflow */
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #6a0dad;
            font-family: Arial, sans-serif;
        }

        .login-box {
            background: white;
            padding: 40px;
            border-radius: 10px;
            width: 300px;
            text-align: center;
        }

        .login-box h2 {
            margin-bottom: 20px;
        }

        .input-group {
            position: relative;
            margin-bottom: 20px;
            width: 100%;
        }

        .input-group input {
            width: 100%;
            padding: 10px;
            padding-right: 45px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .toggle-password {
            position: absolute;
            right: 12px;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            color: #e91e63;
            font-size: 22px;
        }

        .login-btn {
            width: 100%;
            padding: 10px;
            background: green;
            color: white;
            border: none;
            border-radius: 20px;
            cursor: pointer;
        }

        .login-btn:hover {
            background: darkgreen;
        }

    </style>
</head>

<body>

    <div class="login-box">
        <h2>Login</h2>

        <div class="input-group">
            <input type="email" placeholder="Email">
        </div>

        <div class="input-group">
            <input type="password" id="password" placeholder="Password">
            <span class="material-icons toggle-password" onclick="togglePassword()" id="eyeIcon">
                visibility
            </span>
        </div>

        <button class="login-btn">Login</button>
    </div>

    <script>
        function togglePassword() {
            const passwordField = document.getElementById("password");
            const eyeIcon = document.getElementById("eyeIcon");

            if (passwordField.type === "password") {
                passwordField.type = "text";
                eyeIcon.textContent = "visibility_off";
            } else {
                passwordField.type = "password";
                eyeIcon.textContent = "visibility";
            }
        }
    </script>

</body>
</html>
