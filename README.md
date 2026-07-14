# Ledger — To-Do & Notes App

A single-page React app that combines a task ledger and an index-card notes
board, built for the "To-Do App + Notes App" React.js project brief.

## Tech

- React.js (function components + hooks)
- Modern JavaScript (ES6+: arrow functions, destructuring, array methods, modules)
- Plain CSS3 (custom properties, flexbox, grid, responsive breakpoints)

## Features

**Tasks tab**
- Add new tasks
- Mark tasks complete / incomplete
- Delete tasks
- Filter by All / Active / Done
- Live count of remaining tasks

**Notes tab**
- Create notes (title + body)
- Edit notes in place
- Delete notes
- Notes displayed as a responsive index-card grid

## Getting started

```bash
npm install
npm start
```

This runs the app in development mode at [http://localhost:3000](http://localhost:3000).

To create a production build:

```bash
npm run build
```

## Project structure

```
src/
  index.js               # React entry point
  index.css              # global resets + design tokens
  App.js                 # top-level state + tab switching
  App.css                # app shell / folder-tab nav styling
  components/
    TabNav.js             # folder-tab style navigation
    TodoApp.js             # tasks feature (state + logic)
    TodoItem.js            # single task row
    NotesApp.js             # notes feature (state + logic)
    NoteCard.js              # single note card (view + edit mode)
```

## Notes for students

- All shared UI tokens (colors, fonts, spacing) live in `src/index.css` as
  CSS custom properties — change them there to re-theme the whole app.
- State is lifted to `App.js` only where it needs to be shared (the tab); the
  todo list and notes list each manage their own state locally with `useState`,
  which is a good example of component-level state vs. lifted state.
- `TodoItem` and `NoteCard` are intentionally split out as reusable, "dumb"
  presentational components that receive data and callbacks via props.
