# Class Compass 2.1 — Smart Shortcuts & Recurring Plans

Replace the existing `index.html` in the **class-compass** GitHub repository. This is a standalone replacement, not a Learning Hub update. No dependencies or build step. Keep the same GitHub Pages URL and browser origin.

## New in 2.1
- Twelve common subject presets in Settings, with automatic suggested colors and custom subject names still supported. Existing subjects are recognized by name; no setup redo required.
- One-tap daily activity chips, subject-specific suggestions, and frequently used preset shortcuts sorted to the front. Assignment, project, quiz/test, and reminder presets open the quick form for an optional due date.
- Per-period saved shortcuts, editable from My shortcuts & repeats. Save a shortcut directly from the quick-entry form, or create a scheduled plan with school-day, weekly, or selected-weekday recurrence and an explicit start/end date (up to one year).
- Scheduled plans appear on the daily page and calendar until recorded or skipped. They do not count as actual daily entries or create overdue assignments automatically. For task types, optionally choose to create a same-day due task when adding the occurrence. Repeats skip weekends and known no-school dates, respect known first/last days of the selected school year, and are scoped to the selected term and period. Reconfigure for a new term if needed.
- Continue previous work, copy the previous school day's daily activities without duplicating assignments, plan any recorded daily activity for the next school day or next week, and mark only empty periods No homework. The bulk action excludes periods with pending plans or active assignments.
- Shortcuts, usage counts, and scheduled plans are included in the existing local backup format. No new sign-in, network dependency or storage key. Old data remains compatible.

## Retained from 2.0
- Quick mode by default: weekday navigation, direct period entry, large activity choices, optional deadline, no-homework shortcut, repeat previous activity, daily recording progress and checkboxes.
- Detailed mode: original planner plus focus recommendations, estimated workload, planned work dates, estimated/actual minutes, resource URLs, prerequisite references, correction flags, finite repeat series, six project checklist templates, focus/break/stopwatch timers, optional bell countdown, 80 tiered achievements, personal activities, reflection and configurable tools. 
- Weekly reports include daily recording metrics and reflections. Daily activities do not create overdue assignments. Weekly metrics use current class list; logged minutes are cumulative across overlapping assignments, not exclusively minutes logged during the selected week.
- Original storage keys and schema preserved; daily activity and options are additive fields. The original demo/personal separation, school calendars, archives, and backup/import remain. New entries/settings are included in backups; archives include daily activity and settings.

## Before deployment
Ask students to export a backup before refreshing. Upload the replacement to the existing repository root. Commit, allow GitHub Pages to deploy, then refresh. Same-browser data should remain available, but backing up is advisable. No account, server, or cross-device sync. A new device needs an imported backup.

## Validation and limits
JavaScript syntax checked. Chromium DOM smoke tests using simulated local storage passed for demo setup, presets, duplicate prevention, shortcut creation, daily/weekly/custom repeats, holiday skipping, adding same-day tasks, copying to the next school day, skip occurrence, subject settings, calendar indicators and navigation, report rendering, mode switching, and initializing a new page from serialized saved state. Previous 2.0 features are retained in the source; not every prior feature was retested in this release. Browser navigation was blocked in the testing environment, so tests used in-memory HTML and simulated storage rather than a live origin. Live GitHub Pages and actual Chromebook storage were not tested. Bell countdown uses manually entered daily class times and the local clock; rotating schedules, notifications outside the page, actual file attachments, and dedicated distraction-free task screen are not included. Resource links are supported. Achievements are derived from current saved records and are not independent verification. Reports are student-entered records, not proof of time or submission. 
