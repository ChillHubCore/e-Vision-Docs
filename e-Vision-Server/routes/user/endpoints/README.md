# Endpoints For

## user Entity

### POST /signin

This endpoint is used to log in a user. It returns an auto-generated hash token which lasts for a short period to keep them logged in.

**Request Body:**

- `email`: The email of the user.
- `password`: The password of the user.

**Response:**

- `name`: The name of the user.
- `token`: The auto-generated hash token.

### POST /signup

This endpoint is used to sign up a new user. The password is stored in a hashed format. It returns an auto-generated hash token which lasts for a short period to keep them logged in.

**Request Body:**

- `name`: The name of the user.
- `email`: The email of the user.
- `phone`: The phone number of the user.
- `password`: The password of the user.

**Response:**

- `name`: The name of the user.
- `token`: The auto-generated hash token.

### DELETE /:id

This endpoint is used to delete a non-admin user from the database if they exist.

**Path Parameters:**

- `id`: The ID of the user.

**Response:**

- `message`: A message indicating whether the user was deleted or not found.
