# Super Calculator

## Project overview
An Angular 19 calculator app built for teaching purposes. Students implement three intentionally empty methods and write missing unit tests to complete the project.

## Tech stack
- Angular 19 (standalone components)
- TypeScript 5.7
- Karma + Jasmine for unit tests

## How to run
- Install: `npm install`
- Dev server: `npm start` → http://localhost:4200
- Tests: `npx ng test --watch=false --browsers=ChromeHeadless`

## Project structure
- `src/app/app.component.ts` — all calculator logic (state + button handlers)
- `src/app/app.component.html` — template with Angular event bindings
- `src/app/app.component.css` — scoped styles including light/dark theme overrides
- `src/app/app.component.spec.ts` — Karma/Jasmine unit tests

## Exercises
Three methods were intentionally left empty as student exercises (all now implemented):
1. `pressToggleSign()` — flips sign of displayed number (`5` → `-5`)
2. `pressPercent()` — divides displayed number by 100 (`50` → `0.5`)
3. `toggleTheme()` — toggles `isLightMode` boolean; CSS light mode rules are in `app.component.css`

## Coding conventions
- All calculator state lives as properties on `AppComponent`
- Display value is always stored as a `string`; use `parseFloat()` to operate on it
- Call `fixture.detectChanges()` after any state change in tests before querying the DOM
