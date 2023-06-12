# Alisas Portfolio

Welcome! This is the codebase for Alias Portfolio.

## Prerequisites

To get started with this project, make sure you have the following software installed on your machine:

- [Node.js](https://nodejs.org/en/)

## Getting Started

1. Download the repository to your local machine or clone it using the following command:

```bash
git clone https://github.com/your-username/project-name.git
```

2. Navigate to the project's directory:

```bash
cd alisa
```

3. Install the project dependencies:

```bash
npm install
```

4. Start the development server:

```bash
npm run dev
```

This will launch the SvelteKit development server and you should see a message indicating the server is running. By
default, the server runs on http://localhost:8080.
Open your web browser and visit http://localhost:8080 to see your SvelteKit application in action.

## Project Structure

Here's a quick overview of the project's structure and important files:

- **build** - This directory contains the production build of your project. This directory is generated when you run
  the npm run build command.
- **src**
    - **lib** - This directory contains any JavaScript modules that you want to import and use in your application.
    - **routes** - This directory contains the routes for your application. Each route is defined in a separate file.
- **static** - This directory contains any static assets that you want to use in your application, such as images,
  fonts, and CSS files.
- **package.json** - This file contains the project's dependencies and scripts. You can add additional dependencies
  using the npm install command and additional scripts using the npm run command.

When you're ready to build your project for production, use the following command:

```bash
npm run build
```

This will generate a production-ready build in the build directory. You can then deploy the contents of this directory
to your web server.

## Feedback and Support

If you have any questions, feedback, or need support, please contact [@KaiserRuben](https://github.com/KaiserRuben).

Happy coding!