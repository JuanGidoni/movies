# 🎬 My Movies App

> Frontend Engineer Technical Challenge  
> React + Vite + TypeScript + Hexagonal Architecture

---

## 🚀 Project Overview

This project is a **scalable, modular and testable React application** designed as a technical challenge to demonstrate:

- ✅ **Scalability** — modular folder structure (Hexagonal Architecture)
- ✅ **Separation of Concerns** — Domain, Application, Infrastructure, and UI
- ✅ **SSR-ready** — built with Vite
- ✅ **Type Safety** — TypeScript
- ✅ **Unit Testing** — Jest + React Testing Library
- ✅ **Clean UI Layer** — BEM SCSS, no CSS-in-JS
- ✅ **Dependency Injection** — mockable repositories context

The app integrates with [The Movie Database API](https://www.themoviedb.org/) and lets users:

- Browse movies by category (Action, Comedy, Horror)
- View movie details
- Add/remove movies to/from a Wishlist

---

## 🗂️ Project Structure

```
src/
├── domain/ # Entities, Repositories Interfaces, ValueObjects
├── application/ # Use Cases
├── infrastructure/ # API Clients, Repositories Implementations
├── presentational/ # UI Components, Pages, Context, Hooks
├── styles/ # SCSS 7-1 Pattern
├── tests/ # Mocks and Setup
```

✔ **Hexagonal Lightweight** — Clean separation of core domain vs infrastructure vs UI.  
✔ Easy to swap real/mocked repositories with `RepositoriesContext`.

---

## ⚙️ Tech Stack

- **React** (with TypeScript)
- **Vite** (fast build, SSR-ready)
- **SCSS** (BEM, no CSS Modules)
- **Jest + React Testing Library** (unit tests)
- **TMDB API** for movie data

---

## 🚩 Prerequisites

- **Node.js** >= 18
- **npm** or **pnpm**
  Create a `.env` file:
  ```env
  VITE_TMDB_API_KEY=your_tmdb_api_key
  VITE_TMDB_API_URL=https://api.themoviedb.org/3
  ```

---

## 🚀 Getting Started

```bash

# Install dependencies

npm install

# Run locally (default: development)

npm run dev

# Run with mock repositories

npm run dev:mock

# Build for production

npm run build

# Preview production build

npm run preview
```

---

## ✅ Running Tests

```bash

# Unit tests with Jest

npm run test
```

Tests cover:

- `useCases` (fetch, add/remove wishlist)
- Infrastructure repositories (mock vs real)
- UI components (`MovieCard`, `Carousel`, `Button`)
- Pages (`HomePage`)

---

## 🎨 SCSS Conventions

- Follows **7-1 Pattern**: base, components, pages, themes.
- Uses `@forward` and `@use` instead of deprecated `@import`.
- BEM naming: `.movie-card`, `.carousel-track`, `.home-page__section`.

---

## 📌 Architecture Decisions

✔ Uses **Dependency Injection** (`RepositoriesContext`) — easily switch between real API and mock repos.  
✔ `useCases` are pure functions — reusable, testable, and independent of UI.  
✔ Context for `Wishlist` state — global and persistent.  
✔ Hooks (`useHomePageLogic`, `useMovieDetailPageLogic`) separate orchestration from rendering.

---

## 🙌 Author

This project is part of a **Frontend Engineer Challenge**  
crafted with ❤️ for scalable, maintainable and testable React apps.

---

## License

Proprietary — All rights reserved.  
This code may not be copied, modified or distributed without explicit permission.

<sub> This readme will change in future commits. <br/> This is a POC and still in progress.</sub>
