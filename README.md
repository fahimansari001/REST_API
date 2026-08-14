# REST Class - Express.js Posts Application

A simple REST-style web application built with **Node.js and Express.js**.
This project demonstrates CRUD operations for posts using Express routes, EJS templates, UUIDs, and HTTP method overriding.

## 🚀 Features

* View all posts
* Create a new post
* View a single post
* Edit an existing post
* Update post content
* Delete a post
* Generate unique IDs using UUID
* Use EJS for dynamic HTML pages
* Use `method-override` for PATCH and DELETE requests

## 🛠️ Technologies Used

* Node.js
* Express.js
* EJS
* UUID
* Method-Override
* HTML/CSS
* JavaScript

The project dependencies include Express, EJS, method-override, and UUID.

## 📁 Project Structure

```text
REST-Class/
│
├── index.js
├── package.json
├── package-lock.json
│
├── views/
│   ├── index.ejs
│   ├── new.ejs
│   ├── show.ejs
│   └── edit.ejs
│
└── public/
    └── CSS / Static Files
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd REST-Class
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the server

```bash
node index.js
```

The application runs on:

```text
http://localhost:8080
```

## 🔗 Routes

| Method | Route             | Description                |
| ------ | ----------------- | -------------------------- |
| GET    | `/posts`          | Display all posts          |
| GET    | `/posts/new`      | Show form to create a post |
| POST   | `/posts`          | Create a new post          |
| GET    | `/posts/:id`      | Display a specific post    |
| GET    | `/posts/:id/edit` | Show edit form             |
| PATCH  | `/posts/:id`      | Update a post              |
| DELETE | `/posts/:id`      | Delete a post              |

The application stores posts in an in-memory JavaScript array and assigns each post a unique UUID.

## 📝 CRUD Operations

### Create

A new post is created using:

```text
POST /posts
```

The username and content are received from the request body and added to the posts array.

### Read

All posts can be viewed at:

```text
GET /posts
```

A single post can be viewed using:

```text
GET /posts/:id
```

### Update

A post can be edited using:

```text
PATCH /posts/:id
```

### Delete

A post can be deleted using:

```text
DELETE /posts/:id
```

## 🔑 Important Packages

### Express

Used to create the web server and handle HTTP routes.

### EJS

Used as the template engine for rendering dynamic pages.

### UUID

Used to generate unique IDs for posts.

### Method-Override

Allows HTML forms to send HTTP methods such as `PATCH` and `DELETE`, which are not directly supported by standard HTML forms.

## 💾 Data Storage

Currently, posts are stored in a JavaScript array:

```javascript
let posts = [
    {
        id: uuidv4(),
        username: "fahim ansari",
        content: "i love coding"
    }
];
```

Because the data is stored only in memory, posts will be lost whenever the server is restarted.

## 📌 Future Improvements

* Add MongoDB or MySQL database
* Add user authentication
* Add post likes and comments
* Add validation for post data
* Add better error handling
* Add responsive UI
* Add search and filtering
* Deploy the application online

## 👨‍💻 Author

**Fahim Ansari**

## 📄 License

This project is licensed under the ISC License.
