# Role Based Access Control (RBAC) - Mini Backend

This project is a mini backend implementation of Role Based Access Control (RBAC) for web development. It provides a simple and efficient way to manage user roles and permissions within your application.

## Use Case

The RBAC system is used to restrict access to certain parts of your application based on the user's role. For example, an admin user might have access to all parts of the application, while a regular user might have limited access. This ensures that users can only perform actions that they are authorized to do, enhancing the security and integrity of your application.

## Features

- Define roles and permissions
- Assign roles to users
- Check user permissions
- Middleware for role-based access control

## Getting Started

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/role-based-access-control-mini-backend.git
    ```
2. Navigate to the project directory:
    ```sh
    cd role-based-access-control-mini-backend
    ```
3. Install the dependencies:
    ```sh
    npm install
    ```

### Usage

1. Start the server:
    ```sh
    npm start
    ```
2. The server will be running on `http://localhost:3000`.

### API Endpoints

- `POST /login` - Authenticate a user and get a token
- `GET /users` - Get a list of users (admin only)
- `POST /users` - Create a new user (admin only)
- `GET /roles` - Get a list of roles (admin only)
- `POST /roles` - Create a new role (admin only)

### Example

To protect a route with RBAC, use the middleware provided:

```javascript
const { authorize } = require('./middleware/authorize');

app.get('/admin', authorize('admin'), (req, res) => {
    res.send('Welcome, admin!');
});
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For any questions or suggestions, please contact [your email].
