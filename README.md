# Proven Performance Ltd — Company Website

A corporate website for **Proven Performance Ltd**, a management and ICT consulting firm based in Abuja, Nigeria. The site presents the company's services, company profile, mission and values, and a contact form for prospective clients.

---

## Live Site

Deployed via **Netlify** → *([Proven Performance Ltd](https://provenperformanceltd.com/))*

---

## Pages

| Route | Page |
|---|---|
| `/` | Home |
| `/about` | About Us |
| `/services` | Services |
| `/contact` | Contact |

---

## Tech Stack

| Technology | Purpose |
|---|---|
| [Vue.js 3](https://vuejs.org/) | JavaScript UI framework |
| [Vue Router 4](https://router.vuejs.org/) | Client-side page routing |
| [Vite](https://vitejs.dev/) | Development server and build tool |
| [Bootstrap 5](https://getbootstrap.com/) | Responsive grid and utility classes |
| [Bootstrap Icons](https://icons.getbootstrap.com/) | Icon library |
| [Netlify](https://netlify.com/) | Hosting and deployment |

---

## Project Structure

```
├── public/                  # Static files served as-is (favicon, etc.)
├── src/
│   ├── assets/              # Images used across the site (logo, hero, team, etc.)
│   ├── components/
│   │   ├── NavBar.vue       # Reusable top navigation bar
│   │   └── FooterView.vue   # Reusable footer with address, links, and social icons
│   ├── views/
│   │   ├── HomeView.vue     # Home page
│   │   ├── AboutView.vue    # About page
│   │   ├── ServicesView.vue # Services page
│   │   └── ContactView.vue  # Contact page with enquiry form
│   ├── router/
│   │   └── index.js         # Route definitions (maps URLs to page components)
│   ├── App.vue              # Root component — mounts the router
│   └── main.js              # Application entry point — boots Vue
├── App.vue
├── index.html               # Single HTML file the app is injected into
├── vite.config.js           # Vite build configuration
├── package.json             # Project dependencies and scripts
└── netlify.toml             # Netlify deployment configuration
```

---

## Key Files Explained

### `main.js`

This is the **entry point** of the entire application. It is the first JavaScript file that runs when the site loads.

```js
import { createApp } from 'vue'
import App from './App.vue'
import router from './router'

createApp(App).use(router).mount('#app')
```

In plain terms:

1. It imports Vue and the root `App.vue` component.
2. It imports the router (the system that maps URLs to pages).
3. It creates a Vue application instance, tells it to use the router, and **mounts** (attaches) it to the `<div id="app">` element inside `index.html`.

Everything visible on the site flows from this one file. Without it, nothing renders.

---

### `App.vue`

This is the **root component** — the outermost shell that every page lives inside. Its template contains just one line of meaningful markup:

```vue
<template>
  <RouterView />
</template>
```

#### What is `<RouterView />`?

Think of `<RouterView />` as a **placeholder** or a window. When a visitor navigates to `/about`, Vue Router looks at the current URL, finds the matching page component (`AboutView.vue`), and renders it inside that placeholder — without reloading the page.

So the flow is:

```
User visits /about
    → App.vue renders
        → <RouterView /> is replaced by AboutView.vue
            → AboutView renders NavBar, its content, and FooterView
```

This is what makes the site a **Single Page Application (SPA)** — the browser loads one HTML file once, and Vue swaps content in and out as the user navigates, making transitions fast and seamless.

---

### `router/index.js`

This file defines the **mapping between URLs and page components**. It is the site's internal directory.

```js
import { createRouter, createWebHistory } from 'vue-router'
import HomeView from '../views/HomeView.vue'

const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [
    { path: '/',         component: HomeView },
    { path: '/about',    component: () => import('../views/AboutView.vue') },
    { path: '/services', component: () => import('../views/ServicesView.vue') },
    { path: '/contact',  component: () => import('../views/ContactView.vue') },
  ]
})

export default router
```

Key points:

- `createWebHistory` gives the site clean URLs (`/about` instead of `/#/about`).
- `() => import(...)` is **lazy loading** — page components are only downloaded by the browser when that page is actually visited, keeping initial load times fast.
- This router is imported into `main.js` and attached to the Vue app with `.use(router)`.

---

### `vite.config.js`

[Vite](https://vitejs.dev/) is the **build tool** — it does two jobs:

1. **During development**: runs a fast local server with instant hot-reloading (changes appear in the browser without a full refresh).
2. **For production**: bundles, minifies, and optimises all the JavaScript, CSS, and assets into static files ready to be deployed.

```js
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  plugins: [vue()],
})
```

The `@vitejs/plugin-vue` plugin teaches Vite how to understand and compile `.vue` files (which standard browsers cannot read natively — they must be compiled to plain JavaScript first).

---

### `package.json`

This is the **project manifest** — a configuration file that Node.js and npm use to understand the project. It lists:

- The project name and version.
- **`dependencies`** — packages required for the site to run in production (Vue, Vue Router).
- **`devDependencies`** — packages only needed during development and building (Vite, the Vue plugin).
- **`scripts`** — shortcut commands:

```json
"scripts": {
  "dev":     "vite",          // Start local development server
  "build":   "vite build",    // Compile the site for production
  "preview": "vite preview"   // Preview the production build locally
}
```

When Netlify deploys the site, it runs `npm run build` to generate the final static files.

---

### `netlify.toml`

This file tells **Netlify** how to build and serve the site. It sits in the project root and is read automatically on every deployment.

```toml
[build]
  command = "npm run build"
  publish = "dist"

[[redirects]]
  from = "/*"
  to   = "/index.html"
  status = 200
```

#### What is Netlify?

[Netlify](https://www.netlify.com/) is a **hosting and deployment platform** designed for modern frontend projects. Key features used here:

- **Automatic deploys**: Connect your GitHub repository and Netlify will automatically rebuild and redeploy the site every time you push a commit to the main branch.
- **Global CDN**: Your built files are distributed across servers worldwide, so the site loads quickly for visitors regardless of their location.
- **HTTPS by default**: Netlify provides a free SSL certificate automatically.
- **No server required**: Since this is a Vue SPA compiled to static files, there is no backend server to manage. Netlify simply serves the files.

#### The redirect rule explained

Because this is a Single Page Application, every URL (`/about`, `/services`, etc.) is handled by JavaScript inside the browser — they are not real files on the server. If a visitor refreshes the page on `/about` or shares that link directly, the server would return a 404 error because there is no actual `about.html` file.

The redirect rule fixes this:

```toml
[[redirects]]
  from = "/*"
  to   = "/index.html"
  status = 200
```

This tells Netlify: *"For any URL that is requested, serve `index.html` with a 200 OK status."* Vue Router then reads the URL inside the browser and renders the correct page. The `status = 200` (rather than 301/302) ensures it is a silent rewrite, not a redirect — the URL in the browser bar stays unchanged.

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) version 18 or higher
- npm (comes bundled with Node.js)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

The site will be available at `http://localhost:5173` by default. Changes to any `.vue` file will appear in the browser instantly without a page reload.

### Building for Production

```bash
npm run build
```

This compiles the project into the `dist/` folder. The contents of `dist/` are what Netlify (or any static host) serves to visitors.

---

## Deployment

The project is configured for **automatic deployment via Netlify**:

1. Push your code to GitHub.
2. Connect the repository to a Netlify account at [app.netlify.com](https://app.netlify.com).
3. Netlify reads `netlify.toml` and runs `npm run build` automatically.
4. The `dist/` folder is deployed to the Netlify CDN.

Every subsequent push to the main branch triggers a new deployment automatically.

---

## Reusable Components

Two components are shared across all pages:

| Component | Description |
|---|---|
| `NavBar.vue` | Fixed top navigation bar. Collapses to a hamburger menu on mobile screens below 992px (Bootstrap `lg` breakpoint). |
| `FooterView.vue` | Site footer containing the office address, quick links, social media icons, and copyright notice. Also includes the "Ready to Transform Your Business?" CTA section above the footer. |

Both are imported and registered individually in each page view that uses them.

---

## Notes for Developers

- **Global CSS variables** such as `--navy`, `--gold`, `--gray`, and `--white` are defined in a global stylesheet and used throughout all components. Ensure this stylesheet is imported in `main.js` for variables to resolve correctly.
- **`<style scoped>`** is used on all components, meaning CSS rules only apply to the component they are written in and will not leak into other components.
- **`fadeInUp` animation** is referenced in hero sections across all pages. Ensure the `@keyframes fadeInUp` rule is defined globally (it is currently defined inside `HomeView.vue` — consider moving it to a global stylesheet so all pages can access it reliably).
- The **contact form** in `ContactView.vue` currently uses `console.log` and an `alert` for form submission feedback. Before going live, replace this with a real form handling service such as [Netlify Forms](https://docs.netlify.com/forms/setup/), [Formspree](https://formspree.io/), or a custom backend API endpoint.
- The `@click` event on the `<form>` element in `ContactView.vue` should be corrected to `@submit` for reliable form submission behaviour across all browsers and input methods.

---

## License

© 2025 Proven Performance Ltd. All rights reserved.