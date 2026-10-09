# CompareX UI

Frontend interface for [CompareX](https://github.com/Akshay-343/comparex) — upload two Excel files, pick a reconciliation config, and download a color-highlighted diff report.

---

## Stack

- **React 19** + **TypeScript**
- **Vite** — dev server and build
- **Tailwind CSS** + **shadcn/ui** — component library
- **Radix UI** — accessible primitives
- **Lucide React** — icons
- **Geist** — font

---

## Getting Started

```bash
npm install
npm run dev
```

Requires the [CompareX engine](https://github.com/Akshay-343/comparex) running locally on `http://localhost:8000`.

---

## Features (Planned / In Progress)

- Drag-and-drop file upload for left and right Excel datasets
- Config selector (fetched live from `/api/configs`)
- Progress feedback during reconciliation
- Inline preview of diff results
- One-click download of the highlighted Excel report
- Run history with previous report downloads

---

## Project Structure

```
src/
  components/       # UI components (upload, config picker, results)
  pages/            # Route-level views
  lib/              # API client, utilities
```

---

## API

This UI talks to the CompareX FastAPI backend:

| Endpoint | Description |
|----------|-------------|
| `GET /api/configs` | fetch available reconciliation configs |
| `POST /api/reconcile` | upload files + run comparison |
| `GET /api/download/{run_id}` | download result report |

---

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | start dev server |
| `npm run build` | production build |
| `npm run lint` | run ESLint |
| `npm run preview` | preview production build |
