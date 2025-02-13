# HTM-Project-1
Creating a simple HTML landing page with a login form that uses a Gmail ID and password involves creating a basic form. However, it's important to note that handling user authentication securely requires server-side processing (e.g., using PHP, Node.js, or Python) and proper security measures (e.g., HTTPS, hashing passwords). Below is a basic example of an HTML form for a login page:

### HTML Code for Login Page
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .login-container h2 {
            text-align: center;
            margin-bottom: 20px;
        }
        .login-container input[type="email"],
        .login-container input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .login-container input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            border: none;
            border-radius: 4px;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
        }
        .login-container input[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login with Gmail</h2>
        <form action="/login" method="POST">
            <label for="email">Gmail ID:</label>
            <input type="email" id="email" name="email" placeholder="Enter your Gmail ID" required>

            <label for="password">Password:</label>
            <input type="password" id="password" name="password" placeholder="Enter your password" required>

            <input type="submit" value="Login">
        </form>
    </div>
</body>
</html>
```

### Explanation:
1. **Form Fields**:
   - `email`: Input field for the user's Gmail ID.
   - `password`: Input field for the user's password.

2. **Form Action**:
   - The `action="/login"` attribute specifies where the form data will be sent when submitted. You need to replace `/login` with the actual server-side endpoint that handles the login process.

3. **Styling**:
   - Basic CSS is used to style the form and make it visually appealing.

### Important Notes:
- **Server-Side Handling**: This HTML form only collects user input. You need a backend (e.g., Node.js, PHP, Python) to validate the credentials and authenticate the user.
- **Security**: Never handle sensitive data like passwords in plain text. Always use HTTPS and hash passwords using libraries like bcrypt.
- **Gmail Integration**: If you want users to log in using their Gmail accounts, consider using **Google OAuth** instead of a traditional login form. This is more secure and user-friendly.

### Google OAuth Integration
For Gmail-based login, it's better to use Google's OAuth 2.0 API. Here's a high-level overview:
1. Register your application in the [Google Developer Console](https://console.developers.google.com/).
2. Use the Google Sign-In button to allow users to log in with their Gmail accounts.
3. Handle the OAuth response on your server to authenticate the user.