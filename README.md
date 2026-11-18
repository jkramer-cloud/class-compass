# Class Compass v2.4 — Shared School Profile

Class Compass retains its v2.3 class countdown, quick shortcuts, recurring plans, weekly reports, and simplified navigation. No Learning Hub change is needed.

## Shared School Profile

Both apps store a versioned schedule under `playforge.sharedSchoolProfile.v1` in browser-local storage. Both must be served from the same exact origin (for example `https://jkramer-cloud.github.io`) and run in the same browser profile. Each app must be connected separately. No server, account, or Google login is required. This is not cross-device cloud synchronization.

### Connect once
1. Export your current app-specific backups first. Upload the replacement `index.html` and `README.md` to each app's existing repository.
2. Open the app with the schedule you want to keep. Save any edits first. In Class Compass, go to **Settings → Shared School Profile**; in Class Tempo, go to **School Day → Set up / edit my day → Shared School Profile**.
3. Click **Share my saved schedule** and confirm. This publishes that saved schedule to the browser's shared profile.
4. Open the other app, go to its Shared School Profile panel, and select **Use shared schedule**. Confirm the selection. Class Compass needs a personal planner with matching school year and term (if specified); demo mode never connects.
5. Subsequent saved schedule edits sync automatically when the other app is not in an edit dialog. If an edit is open, a pending-update notice is shown. If both apps edited the schedule, neither version is silently overwritten: choose **Use shared schedule** to accept the shared version or **Share my saved schedule** to replace it.

### Shared fields and limits
- Period count (4–8), subject names, per-period grade assignments or prep, class colors, lunch group, school year, planner term, preset/custom bell times, and supported school-calendar dates. NVMS preset has seven scheduled periods; use custom times for a different period count. Custom times do not insert a separate lunch block automatically. No rotating or 1/D-day schedule is supplied.
- Only school-calendar dates from the built-in or explicitly imported shared profile are shared. Personal calendar events, teacher/student name fields, assignments, reports, project checkpoints, warm-up tasks, scenes, activity timers, and planner records remain app-specific. Do not include private identifiers in class names. Same-origin storage is not a confidential data vault.
- A new term/year in Class Compass pauses synchronization until the matching profile is connected or a new saved schedule is intentionally published. There is one active shared profile per browser, not multiple simultaneous users or schedules. A teacher profile may contain mixed per-period grades; the planner preserves those. Only NVMS 2026–27 preset bell times are verified; later years require custom or verified bell times. Calendar warnings are advisory, not official school notices.
- **Disconnect** preserves the current local copy and stops updates in that app. The other app remains connected to the shared profile until disconnected separately.
- **Export profile** downloads schedule-only JSON; **Import profile** explicitly activates a shared profile on another browser. Keep each app's regular backup too. Restoring a full app backup disconnects shared sync before restoring the local data. Files opened directly from disk may not share storage; test using the deployed GitHub Pages URLs.

### Validation
JavaScript syntax, Chromium with simulated same-origin shared storage and storage events, two-way transfer, mixed grades, custom times, colors, pending conflicts, disconnection, reload, and demo isolation tested. Class Compass's existing live bell countdown regression also passed. Browser hosting was blocked in the test environment, so deployed GitHub Pages and real school Chromebook validation remain outstanding. No live repositories were changed.

---

# Class Compass v2.3 — Live class countdown

## What changed
- Compact Class Tempo-style countdown in the top header on every planner page. On desktop the header stays visible while scrolling. The countdown includes the current period/subject, remaining time, next period, a remaining-time bar, two-minute amber warning and final 25-second red warning. No audio or notifications.
- The exact 2026–27 NVMS bell times are copied from the existing Class Tempo v2.10 schedule. For grades 5–8, when no manual schedule was previously entered, the preset automatically selects Monday late start or Tuesday–Friday regular and the grade-appropriate lunch. Existing manually entered times are preserved and remain the default when present. Future school years require confirmation/new schedule rather than silently assuming the same times.
- Live device clock controls the countdown (including in demo mode, which is labeled LIVE). Browsing other planner dates never changes the live time. Current school calendar dates are respected, including weekends, breaks and holidays. Known half-days, conferences and tentative snow makeup dates display a schedule warning rather than an unverified countdown. No rotating or 1/D-day times were supplied.
- Click the countdown to configure NVMS auto/day override or custom class times. Overrides persist until changed. Existing Planner options also control whether the countdown appears. Custom schedules are stored locally in the same backup format. Tools uses the same countdown; the separate focus timer remains available.
- Replace index.html and README.md in the existing class-compass repository. No Learning Hub update or new repository needed. Back up existing student data before installing. No external libraries, login or network requests.

## Validation
JavaScript syntax and Chromium simulated-clock tests passed for regular and Monday schedules, both lunch groups, period transitions, warnings, holidays/weekends, half-day warning, completed school day, manual times, persisted settings, day overrides, navigation and desktop/narrow screen header layout. Live deployment and Chromebook testing remain outstanding. The countdown is not an authoritative substitute for school announcements or bells. It uses the device's local clock and the preloaded calendar.

---

# Class Compass v2.2 — One simple planner

## What changed
- Repaired malformed HTML so every navigation page is inside the primary content area.
- Removed the Quick / Detailed toggle; the daily Quick workflow is now the single default.
- Tools contains focus timer, optional bell countdown, priorities, workload, achievements, weekly reflection and the collapsible schoolwork overview.
- Optional personal tasks and assignment details stay available behind expandable sections.
- Existing storage keys, schema, backups, routines, shortcuts and demo data are retained.
- Replace index.html and README.md in the existing repository. No Learning Hub changes required. Export a backup before deployment.

---

## Smart shortcuts & recurring plans (retained from 2.1)

Replace the existing `index.html` in the **class-compass** GitHub repository. This is a standalone replacement, not a Learning Hub update. No dependencies or build step. Keep the same GitHub Pages URL and browser origin.

### Features
- Twelve common subject presets in Settings, with automatic suggested colors and custom subject names still supported. Existing subjects are recognized by name; no setup redo required.
- One-tap daily activity chips, subject-specific suggestions, and frequently used preset shortcuts sorted to the front. Assignment, project, quiz/test, and reminder presets open the quick form for an optional due date.
- Per-period saved shortcuts, editable from My shortcuts & repeats. Save a shortcut directly from the quick-entry form, or create a scheduled plan with school-day, weekly, or selected-weekday recurrence and an explicit start/end date (up to one year).
- Scheduled plans appear on the daily page and calendar until recorded or skipped. They do not count as actual daily entries or create overdue assignments automatically. For task types, optionally choose to create a same-day due task when adding the occurrence. Repeats skip weekends and known no-school dates, respect known first/last days of the selected school year, and are scoped to the selected term and period. Reconfigure for a new term if needed.
- Continue previous work, copy the previous school day's daily activities without duplicating assignments, plan any recorded daily activity for the next school day or next week, and mark only empty periods No homework. The bulk action excludes periods with pending plans or active assignments.
- Shortcuts, usage counts, and scheduled plans are included in the existing local backup format. No new sign-in, network dependency or storage key. Old data remains compatible.

## Retained from 2.0
- Daily planner: weekday navigation, direct period entry, large activity choices, optional deadline, no-homework shortcut, repeat previous activity, daily recording progress and checkboxes.
- Optional Tools page and expandable assignment details provide focus recommendations, estimated workload, planned work dates, estimated/actual minutes, resource URLs, prerequisite references, correction flags, finite repeat series, six project checklist templates, focus/break/stopwatch timers, optional bell countdown, 80 tiered achievements, personal activities, reflection and configurable tools. 
- Weekly reports include daily recording metrics and reflections. Daily activities do not create overdue assignments. Weekly metrics use current class list; logged minutes are cumulative across overlapping assignments, not exclusively minutes logged during the selected week.
- Original storage keys and schema preserved; daily activity and options are additive fields. The original demo/personal separation, school calendars, archives, and backup/import remain. New entries/settings are included in backups; archives include daily activity and settings.

## Before deployment
Ask students to export a backup before refreshing. Upload the replacement to the existing repository root. Commit, allow GitHub Pages to deploy, then refresh. Same-browser data should remain available, but backing up is advisable. No account, server, or cross-device sync. A new device needs an imported backup.

## Validation and limits
Prior v2.1 validation: JavaScript syntax checked. Chromium DOM smoke tests using simulated local storage passed for demo setup, presets, duplicate prevention, shortcut creation, daily/weekly/custom repeats, holiday skipping, adding same-day tasks, copying to the next school day, skip occurrence, subject settings, calendar indicators and navigation, report rendering, and initializing a new page from serialized saved state. V2.2: Chromium verified all seven navigation pages show independently inside the main area, reset scroll, and highlight the active menu. Tested desktop and narrow layout, daily shortcuts, timer across navigation, saving optional assignment estimates, personal log, recurrence/calendar and reloading persisted plans. Not every previous feature was retested. Browser navigation was blocked in the testing environment, so tests used in-memory HTML and simulated storage rather than a live origin. Live GitHub Pages and actual Chromebook storage were not tested. Bell countdown uses manually entered daily class times and the local clock; rotating schedules, notifications outside the page, actual file attachments, and dedicated distraction-free task screen are not included. Resource links are supported. Achievements are derived from current saved records and are not independent verification. Reports are student-entered records, not proof of time or submission. 
