# HTM-Project-1
Creating a simple HTML landing page with a login form that uses a Gmail ID and password involves creating a basic form. However, it's important to note that handling user authentication securely requires server-side processing (e.g., using PHP, Node.js, or Python) and proper security measures (e.g., HTTPS, hashing passwords). Below is a basic example of an HTML form for a login page:

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
