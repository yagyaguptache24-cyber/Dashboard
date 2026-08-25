# Flipspaces Team Dashboard

A lightweight, real-time team and task management board built during my Strategy Internship at Flipspaces. Designed to give a small team quick visibility into who's working on what, task status, and upcoming deadlines — without the overhead of a full project management tool.

## Features

- **Team member management** — add teammates with names, roles, and auto-generated color-coded avatars
- **Task board (Kanban view)** — organize tasks by team member, with drag-free status updates via dropdown (To Do → In Progress → Blocked → Done)
- **Priority tagging** — Low / Medium / High priority labels on every task
- **Timeline view** — visual progress bars for tasks with both a start and due date, with automatic overdue flagging
- **Live sync** — all data is stored in a shared Supabase backend, so multiple teammates see the same board update in real time
- **Zero backend code** — a single self-contained HTML file; no build step, no server to run

## Tech Stack

- **React 18** (loaded via CDN, no bundler)
- **Babel Standalone** for in-browser JSX transpilation
- **Supabase** (Postgres + REST API) for shared, persistent storage
- Plain CSS-in-JS styling — no external UI framework

## How It Works

The entire app lives in one HTML file. On load, it fetches the current board state from a Supabase table (`dashboard`) and polls/pushes updates as changes are made, so it acts like a lightweight real-time multiplayer app.

## Setup

1. Create a free project at [supabase.com](https://supabase.com)
2. Create a table called `dashboard` with a single JSON `data` column and an `id` column
3. Open `team-dashboard.html` and replace the placeholders near the top:
```js
   window.SUPABASE_URL = "YOUR_SUPABASE_URL_HERE";
   window.SUPABASE_ANON_KEY = "YOUR_SUPABASE_ANON_KEY_HERE";
```
4. Open the file directly in a browser — no build or install needed

## Why I
