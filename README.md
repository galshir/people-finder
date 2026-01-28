# people-finder App

people-finder is a small React app that displays a list of people and lets you mark favorites. It was built with Create React App and uses a custom hook to fetch people data, a simple favorites view, and styled-components for styling.

> Project in the repo: galshir/people-finder

## Demo / Icon

The app includes the default CRA icons in the `public/` folder. If you want to show the app icon or screenshots here, you can reference files from `public/`:

- App icon (192x192): `public/logo192.png`  
- App icon (512x512): `public/logo512.png`

Example:
![App Icon](public/logo192.png)

(If you want a full-screen screenshot, run the app locally and replace the image path above with a screenshot you add to `public/screenshots/`.)

## Features

- Fetches and displays a list of users (people).
- Mark/unmark favorites and view a Favorites page.
- Simple, responsive UI built with styled-components.
- Loading spinner while fetching data.

## Project structure (high level)

- public/ — static files (index.html, icons)
- src/
  - pages/
    - Home/ — main listing page (title + user list)
    - Favorites/ — favorites listing page
  - components/ — UI components (UserList, FavoritiesList, Spinner, NavBar, Text, CheckBox, etc.)
  - hooks/ — custom hooks (usePeopleFetch, useFavoritesFetch)
  - AppRouter / index.js — app entry and routing
  - constant.js — size/variant/color constants

Key files I inspected:
- `src/pages/Home/Home.js` — main app entry for the home page (renders `UserList`)
- `src/components/UserList/*` — user list layout and styles
- `src/hooks/usePeopleFetch` — custom hook that controls fetching and loading state
- `public/index.html` — contains the `<title>` and references to `logo192.png`, `logo512.png`, `favicon.ico`

## Getting started (local)

1. Clone the repository
   - git clone https://github.com/galshir/people-finder.git
2. Install dependencies
   - npm install
3. Start the development server
   - npm start
4. Open http://localhost:3000

(If your repo uses Yarn, replace the npm commands with `yarn` / `yarn start`.)

## Available scripts

- `npm start` — start dev server
- `npm run build` — build for production
- `npm test` — run tests (if present)

## How it works (brief)

- The home page uses `usePeopleFetch()` to fetch a list of users and provide `users`, `isLoading`, and `fetchUsers` to the `UserList` component.
- `UserList` renders the list and allows marking items as favorites (favorites persisted where your hook implements it — e.g., localStorage or state).
- The UI styling uses `styled-components` (see `src/components/*/style.js` and `src/pages/*/style.js`).

## Contributing

If you want collaborators:
1. Fork the repo
2. Create a feature branch (git checkout -b feature/my-feature)
3. Commit your changes and open a pull request

Suggestions for improvements:
- Add infinite scroll to the user list (you mentioned this in the repo).
- Add tests for hooks and components.
- Add a settings page with page size or filtering options.

## Notes / TODO

- The original README in the repo contains a note about adding "Infinity Scroll". If you'd like, I can add an implementation plan and issues for adding infinite scrolling (I can draft the issue(s) for you).
- If you want me to extract a screenshot from a running build or generate a sample screenshot using a headless browser, tell me and I can automate that and update the README with the real screenshot path.

## License

Add your preferred license here (e.g., MIT). If you want, I can add an MIT license file.

---

If you want, I can:
- Commit this README to the repository for you.
- Replace the placeholder screenshots with actual screenshots (I can run the app locally or render a screenshot if you want).
- Create issues for TODOs like infinite scroll and tests.

Tell me which of the above you want next and I'll proceed.
