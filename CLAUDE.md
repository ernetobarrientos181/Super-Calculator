# Super Calculator

## Project overview
A beginner-friendly calculator web app built with Angular 19 for teaching purposes. Three methods are intentionally left empty as student exercises, along with missing unit tests to complete.

## Tech stack
- Angular 19 (standalone components)
- TypeScript 5.7
- Karma + Jasmine for unit tests

## How to run
- Install: `npm install`
- Dev server: `npm start` → http://localhost:4200
- Tests: `npx ng test --watch=false --browsers=ChromeHeadless`

## Project structure
- `src/app/app.component.ts` — all calculator logic: state properties and button handler methods
- `src/app/app.component.html` — template with Angular event bindings `(click)` and property bindings `[class]`
- `src/app/app.component.css` — scoped styles; includes empty light mode selectors for Exercise 3
- `src/app/app.component.spec.ts` — Karma/Jasmine unit tests; some are marked `pending()` as student exercises

## Exercises
Three methods were intentionally left empty for students to implement:
1. `pressToggleSign()` — flips the sign of the displayed number (`5` → `-5`, `-3` → `3`)
2. `pressPercent()` — divides the displayed number by 100 (`50` → `0.5`)
3. `toggleTheme()` — toggles `isLightMode`; light mode CSS rules in `app.component.css` also need filling in

## Coding conventions
- All calculator state lives as properties on `AppComponent` (`display`, `firstOperand`, `operator`, `isLightMode`)
- `display` is always a `string`; use `parseFloat()` to convert before arithmetic, `.toString()` to convert back
- In tests, always call `fixture.detectChanges()` after modifying component state before querying the DOM
- No comments describing what the code does — only comments explaining non-obvious constraints or edge cases
