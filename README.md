# JobTracker — Job Application Tracker

A single-page React app for tracking job applications from first click to offer. Sign in with Google to sync across devices via Firebase, or just use it locally without an account.

## Features

- **Kanban Board** — Drag-and-drop cards between columns: Applied, OA, Phone Screen, Technical, Onsite, Offer, Rejected, Ghosted
- **Table View** — Sortable, filterable list with bulk status updates
- **Dashboard** — Stats cards, pie chart (status breakdown), bar chart (applications over time)
- **Google Sign-In** — OAuth via Firebase; your data follows you across devices
- **Offline Mode** — Works without signing in using localStorage
- **Full CRUD** — Add, edit, delete applications through a slide-over form
- **Resume Upload** — Upload PDFs with inline preview
- **Job Description Storage** — Paste JDs so you have them even after listings go dark
- **Search and Filter** — By company/role, status, job type, and date range
- **Import / Export** — JSON and CSV export, JSON import
- **Dark Mode** — Toggles manually or follows system preference
- **Keyboard Shortcuts** — `N` new app, `/` focus search, `Esc` close modals
- **Follow-up Alerts** — Flags applications with no status change in 7+ days
- **Responsive** — Works on desktop and mobile

## Getting Started

```bash
git clone https://github.com/YOUR_USERNAME/job-tracker.git
cd job-tracker
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

## Firebase Setup (Cloud Sync)

To enable Google Sign-In and Firestore sync:

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project
2. Enable **Authentication** → Sign-in method → **Google**
3. Create a **Firestore Database** (test mode is fine to start)
4. Go to **Project Settings** → General → Your apps → Add a **Web app**
5. Copy the config values and create a `.env` file:

```bash
cp .env.example .env
```

Then fill in:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your-project-id
VITE_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=000000000000
VITE_FIREBASE_APP_ID=1:000000000000:web:0000000000000000
```

The app runs without Firebase — just click "Continue without signing in" to use localStorage only.

## Tech Stack

| Tool | Purpose |
|------|---------|
| [React 19](https://react.dev) | UI framework |
| [Vite 8](https://vite.dev) | Build tool and dev server |
| [Tailwind CSS 4](https://tailwindcss.com) | Utility-first styling |
| [Firebase](https://firebase.google.com) | Auth (Google) + Firestore |
| [@hello-pangea/dnd](https://github.com/hello-pangea/dnd) | Drag-and-drop |
| [Recharts](https://recharts.org) | Charts |
| [Lucide React](https://lucide.dev) | Icons |

## Project Structure
