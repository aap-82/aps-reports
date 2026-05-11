aps-reports
Sample report library for Access Property Services Pty Ltd, deployed to Cloudflare Workers as static assets.
Layout
```
.
├── wrangler.jsonc          Worker + static-assets config
└── public/                 Everything served from the worker
    ├── index.html          The showcase landing page
    ├── aps-logo.svg        Brand mark used in the topbar
    └── Final\_Defects\_Inspection\_Report\_\*.html  Live sample report
```
Deploy
The deploy is wired through Cloudflare's Workers Builds, triggered on every push to `main`. Locally:
```bash
npx wrangler deploy
```
Add another sample report
Drop the HTML file into `public/`.
Open `public/index.html`, copy one of the `is-coming` cards, swap the title, description, and tag, and change the surrounding `<div>` to `<a class="report-card" href="./your-new-report.html">` so it becomes clickable.
Optionally change the `report-badge is-soft` to a `report-badge` to mark it Live.
Commit and push.
