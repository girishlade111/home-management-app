# Home Management App

A modern, all-in-one home management dashboard built with Next.js. Manage your smart home, calendar, todos, expenses, meal plans, and household inventory from a single beautiful tabbed interface.

## Features

- **Smart Home** — monitor and control smart home devices and status
- **Calendar** — plan and view household events and schedules
- **Todo List** — track chores and tasks for the household
- **Expense Tracker** — record and review home expenses
- **Meal Planner** — plan weekly meals for the family
- **Inventory** — keep track of household items and supplies
- Dark glassmorphism UI with a tabbed dashboard layout
- Responsive design — works on desktop and mobile

## Tech Stack

- [Next.js](https://nextjs.org/) 15 (App Router, static export)
- [React](https://react.dev/) 19
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) + `tailwindcss-animate`
- [shadcn/ui](https://ui.shadcn.com/) components (Radix UI primitives)
- [Recharts](https://recharts.org/) for charts
- [Lucide](https://lucide.dev/) icons, `date-fns`, `react-day-picker`, `react-hook-form` + `zod`

## Getting Started

```bash
npm install
npm run dev      # start dev server at http://localhost:3000
npm run build    # production build
npm start        # run production build
```

Node.js 18+ recommended. If you hit peer-dependency conflicts during install, use:

```bash
npm install --legacy-peer-deps
```

## Project Structure

```
app/                  # Next.js App Router pages and layout
  page.tsx            # main dashboard with tab navigation
components/           # feature components
  smart-home.tsx      # smart home tab
  calendar.tsx        # calendar tab
  todo-list.tsx       # todo list tab
  expense-tracker.tsx # expense tracker tab
  meal-planner.tsx    # meal planner tab
  inventory.tsx       # inventory tab
  dashboard-header.tsx
  theme-provider.tsx / mode-toggle.tsx
  ui/                 # shadcn/ui primitives
lib/                  # utilities
public/               # static assets
styles/               # global styles
```

## Environment Variables

None required — the app runs fully client-side with no backend or API keys.

## Deployment

The app is statically exported (`output: 'export'` in `next.config.mjs`), so it can be hosted anywhere that serves static files:

```bash
npm run build   # outputs to ./out
```

Notes:

- The repo is synced from a v0.app project and was originally deployed on Vercel as `v0-home-management-app`.
- When deployed under a subpath (e.g. GitHub Pages project pages), `next.config.mjs` sets `basePath: '/home-management-app'`. Remove `basePath` (and keep `output: 'export'`) when deploying to a root domain or Vercel, otherwise assets will resolve incorrectly.

## Built by

Built by Girish Lade — https://ladestack.in
