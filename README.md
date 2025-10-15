HWS notice board — ready-to-deploy Eleventy + Netlify CMS PWA
===========================================================

This repository is a ready-made site for the "HWS notice board".
It uses Eleventy (11ty), Netlify CMS (editorial workflow), and simple PWA support.

How to deploy (quick):
1. Create a new GitHub repository (public) and push the contents of this folder to it.
   - OR upload the ZIP contents via GitHub web UI.
2. On Netlify (https://app.netlify.com) choose "Add new site" -> "Import from Git".
   - Connect your GitHub account and select the repo.
   - Build command: npm run build
   - Publish directory: _site
3. After deploy, enable Identity:
   - Site settings -> Identity -> Enable Identity service
   - Under Identity settings enable Git Gateway
   - Invite yourself (or allow signups) so you can log into /admin
4. Visit https://<your-site>.netlify.app/admin to use the CMS.
   - Create posts, upload images (images stored in /images), set due dates and section.
5. To ensure "Today" and "Past" update automatically each day, create a Netlify Build Hook and a free daily cron (e.g., cron-job.org) that pings the hook once per day.

Key features included:
- Sections: Today (default), Urgent, Notices, Opportunities (permanent toggle), Community (submissions), Past
- Images attached to posts via Netlify CMS (media_folder: images)
- PWA manifest + service worker (basic offline caching)
- London timezone used for date calculations (Europe/London)

Files of interest:
- .eleventy.js               : Eleventy config (collections + timezone)
- admin/config.yml           : Netlify CMS config
- public/manifest.json       : PWA manifest
- public/service-worker.js   : Service worker
- src/_layouts/*.njk         : Layouts and templates
- src/posts/*.md             : Example posts
- images/*                   : Example images

If you want, I can also:
- Create a GitHub repository for you (I cannot do that directly — but I can give exact git commands to run).
- Walk you through enabling Identity/Git Gateway and inviting users.
- Add more polished styling or a different look (e.g., Pico.css or Bulma).

Enjoy — the ZIP file is attached below.