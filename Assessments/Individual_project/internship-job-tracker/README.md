# CareerTrack — Internship & Job Application Tracker

CareerTrack is a responsive React application for students and fresh graduates to organize internship/job applications, deadlines, interviews, company information, and job-search progress.

## Features

- Dashboard summary cards, status chart, monthly activity chart, upcoming deadlines, and interviews.
- Application CRUD: add, edit, delete, search, filter, sort, and update status.
- Application detail pages with notes, timeline, and linked interviews.
- Company directory with application and interview counts.
- Interview scheduling, status management, preparation notes, and feedback.
- Calendar displaying application deadlines and interviews.
- Analytics with status breakdown, interview outcomes, response rate, and conversion estimates.
- Deadline reminders in the in-app notification panel.
- Light/dark theme and editable local demo profile.
- JSON backup import/export and CSV export.
- Local persistence with `localStorage`.

## Technology stack

- React 18
- Vite
- React Router DOM
- Recharts
- Lucide React
- CSS3
- JSON seed data
- Browser `localStorage`

## Run locally

Install Node.js (LTS recommended), then open a terminal in this folder and run:

```bash
npm install
npm run dev
```

Open the local URL printed by Vite, usually `http://localhost:5173`.

To create a production build:

```bash
npm run build
npm run preview
```

## Dummy database and persistence

Initial sample records are stored in:

- `src/data/applications.json`
- `src/data/companies.json`
- `src/data/interviews.json`
- `src/data/notifications.json`

On the first visit, the app uses these JSON records as seed data. User changes are saved in browser `localStorage`; imported JSON modules themselves are not modified by the browser. Use **Settings → Reset sample data** to restore the bundled seed records. Use **Settings → Export full JSON backup** to download current records.

This is a frontend-only academic demo. It has no backend, secure authentication, cloud sync, email/SMS delivery, or server-side database. Data belongs to the current browser profile and can be lost if browser storage is cleared.

## Demo data

The app contains 12 fictional company/application records and six interview examples. Names are fictional sample records for demonstration. Dates are examples and should be updated before a live demo.

## Project structure

```text
internship-job-tracker/
├── index.html
├── package.json
├── README.md
└── src/
    ├── App.jsx
    ├── main.jsx
    ├── data/
    │   ├── applications.json
    │   ├── companies.json
    │   ├── interviews.json
    │   └── notifications.json
    └── styles/
        └── global.css
```

The main UI is kept in `App.jsx` for ease of setup and demonstration. The JSON data and styles are separate and can be further split into feature-specific components as a future enhancement.

## Suggested test checklist

1. Add an application and verify that it appears in the table and dashboard.
2. Edit an application and change its status.
3. Search and filter applications.
4. Delete an application and confirm that linked interviews are removed.
5. Schedule an interview linked to an application.
6. Update an interview status to Completed.
7. Open the calendar and select a date with an event.
8. Review analytics after changing statuses.
9. Refresh the browser and confirm that changes persist.
10. Export JSON/CSV, then test importing a JSON backup.
11. Toggle dark mode and refresh.
12. Reset sample data only after exporting anything you want to keep.

## Future enhancements

- Backend API and database.
- Secure authentication and multi-user support.
- Real email and push notifications.
- Resume and document attachments.
- Interview preparation question bank.
- Cloud synchronization.
- Automated tests and CI pipeline.

## Conclusion

CareerTrack provides a centralized, user-friendly way for students to manage their job-search pipeline. It demonstrates React component composition, routing, CRUD operations, filtering, data visualization, JSON seed data, and browser storage.
