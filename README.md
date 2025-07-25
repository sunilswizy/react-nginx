# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.


## Issue

Run the application locally—you will be able to access it without any issues.

There are two routes added: / and /:id (a dynamic route).
If you try to access both routes locally, they will work as expected.

Next, the same app is deployed using Nginx. I have set up a Dockerfile for it.
Build and run the application with Docker, exposing port 80. You should be able to access the application on port 80.

However, unlike the local setup, when using dynamic routing, paths that overlap with existing folders in the public directory—specifically /assets and /translation—do not work correctly. These folders exist in the public directory, and attempting to access them through dynamic routes fails.

That's the issue. I need help resolving this so that dynamic routing works correctly, and any path entered (including /assets, /translation, etc.) is handled by the app unless it's a request for a static file.

