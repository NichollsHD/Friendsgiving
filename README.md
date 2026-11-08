# Friendsgiving Table

A one-page, live view of the Friendsgiving Dish Sign-Up sheet. Powered by Nicholls Tech.

Everyone keeps signing up in the Google Sheet. This page only reads it: it pulls the Sign-Up and Menu tabs each time it opens and every 60 seconds after that, and shows people signed up, dishes per course, how many servings each course covers, dietary needs (without names), and what's still up for grabs. If the sheet can't be reached it keeps the last version it got and says so.

## Setup

1. In the sheet: Share > General access > "Anyone with the link" > Viewer. (Required: the page reads the sheet without signing in. Anyone with the sheet's link or this page can then see the sign-ups, including the allergy column. Edit rights don't change.)
2. Make a new public GitHub repo, e.g. `friendsgiving`, and add `index.html` to it.
3. Repo Settings > Pages > Deploy from a branch > `main` / root. The page shows up at `https://<your-username>.github.io/friendsgiving/`.

To run it locally instead: `npx serve .` in this folder and open the address it prints.

## Settings

At the top of `index.html`, in `FG_CONFIG`:

- `eventDate`: set it (e.g. `"2026-11-21T17:00"`) to show a countdown.
- `showAllergyNames`: `true` shows who listed each dietary need.
- `refreshSeconds`: how often it re-reads the sheet.
