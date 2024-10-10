# Express Static File Server

This is a basic web server built with Node.js and Express. It serves static HTML files from a "public" directory, handles routing, and includes error handling for 404 and 500 errors. The server also uses environment variables for the port configuration.

## Features

- Serves static files (HTML, CSS, JavaScript, images) from the `public` directory.
- Routes for the homepage (`/`), About page (`/about`), and Contact page (`/contact`).
- Custom 404 page for handling non-existent routes.
- Error handling middleware for server errors (500).

## Prerequisites

- [Node.js](https://nodejs.org/) (v12 or higher)
- [npm](https://www.npmjs.com/)

## Setup

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root of your project and set the following environment variable:

   ```bash
   PORT=8080
   ```

4. Ensure that your `public` directory contains the required HTML files: `index.html`, `about.html`, `contact.html`, and `404.html`.

## Running the Server

Start the server by running:

```bash
npm start
```

By default, the server will run on `http://localhost:8080`. You can change the port by modifying the `PORT` variable in the `.env` file.

## Project Structure

```bash
.
├── public
│   ├── index.html      # Home page
│   ├── about.html      # About page
│   ├── contact.html    # Contact page
│   └── 404.html        # Custom 404 page
├── .env                # Environment variables
├── package.json        # Node.js dependencies and scripts
└── server.js           # Express server code
```

## Routes

- `/` - Serves the `index.html` file (home page).
- `/about` - Serves the `about.html` file.
- `/contact` - Serves the `contact.html` file.
- Any non-existent routes will return the `404.html` page.

## Error Handling

- Custom 404 page for routes that don't exist.
- Middleware for catching server-side errors (500) and sending a custom message.

## License

This project is open-source and available under the [MIT License](LICENSE).
