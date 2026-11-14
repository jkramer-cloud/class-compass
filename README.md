# Class Compass — Student Planner v1.3

A student-first browser planner for Grades 5–12, built for the Naches Learning Hub. No Google sign-in, account, backend, or external libraries are required. The site can run as a single `index.html` on GitHub Pages.

## New in v1.3: Student welcome and onboarding

- On the first visit, students choose **Explore Demo** or **Create My Planner**.
- **Explore Demo** opens fictional Grade 7 assignments and projects dated through November 13, 2026. Demo data is stored separately from personal work.
- **Create My Planner** walks students through Step 1 (name, school year, and grade) and Step 2 (quarter/semester, seven-period class schedule, subject names, teacher names, and customization).
- A name is required to continue from the first personal setup screen; the class-setup step can still be edited later in Settings.
- After approximately **10 minutes of active, visible Demo usage**, a *nonblocking* reminder invites students to make a personal planner. **Keep exploring** dismisses the reminder for that visit. It doesn't appear during the initial choice screen and won't run while the tab is hidden.
- Returning students with previously saved planner data bypass the first-visit choice and reopen where they left off. The prior v1.2 storage and backup formats are unchanged.

## Existing planner features

- 7-period middle-school quarter schedules, high-school semester schedules, and class colors
- Assignments, due dates, follow-up reminders, long-term projects, and checklists
- 2026–27 and 2027–28 Naches Valley calendars (with a noted discrepancy in the second year's printed spring-break dates)
- Weekly downloadable student-name PDF reports; sample reports clearly marked **SAMPLE**
- Browser-local automatic saving; full JSON backup/restore, CSV export, printing, and school-year archives
- Fonts, sizes, and appearance settings

## Publishing

1. Create or open the GitHub repository named `class-compass`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Go to Settings → Pages → Deploy from a branch → `main` and `/ (root)`.
4. After publishing, open `https://jkramer-cloud.github.io/class-compass/` and test it in a fresh browser profile.
5. The Naches Learning Hub already has a Class Compass listing from its v31.50 update; this v1.3 ZIP updates **only the planner repository**, not the Hub.

## Student data and privacy

**Creating a planner does not create an account.** Data is stored only in browser localStorage, so it does not automatically sync between Chromebooks. Managed devices may clear browser storage during sign-out or maintenance. Students should use **Save backup** regularly and keep their exported JSON file in a school-approved location. The weekly report summarizes student-entered changes; it is not independent verification that work was completed.

The 2027–28 school calendar in the supplied district PDF includes conflicting printed and highlighted spring-break dates. Confirm those dates with the district before depending on them.
