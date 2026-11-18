# Class Compass 2.0 — Quick & Detailed Planner

Replace the existing `index.html` in the **class-compass** GitHub repository. This is a standalone replacement, not a Learning Hub update. No dependencies or build step. Keep the same GitHub Pages URL and browser origin.

## What's new
- Quick mode by default: weekday navigation, direct period entry, large activity choices, optional deadline, no-homework shortcut, repeat previous activity, daily recording progress and checkboxes.
- Detailed mode: original planner plus focus recommendations, estimated workload, planned work dates, estimated/actual minutes, resource URLs, prerequisite references, correction flags, finite repeat series, six project checklist templates, focus/break/stopwatch timers, optional bell countdown, 80 tiered achievements, personal activities, reflection and configurable tools. 
- Weekly reports include daily recording metrics and reflections. Daily activities do not create overdue assignments. Weekly metrics use current class list; logged minutes are cumulative across overlapping assignments, not exclusively minutes logged during the selected week.
- Original storage keys and schema preserved; daily activity and options are additive fields. The original demo/personal separation, school calendars, archives, and backup/import remain. New entries/settings are included in backups; archives include daily activity and settings.

## Before deployment
Ask students to export a backup before refreshing. Upload the replacement to the existing repository root. Commit, allow GitHub Pages to deploy, then refresh. Same-browser data should remain available, but backing up is advisable. No account, server, or cross-device sync. A new device needs an imported backup.

## Validation and limits
JavaScript syntax checked; Chromium smoke tests with simulated local storage passed for demo entry, daily logs, due-date assignment, mode switching, detailed task and template, calendar, report rendering, timers and persisted state. Live GitHub Pages and actual Chromebook storage were not tested. Bell countdown uses manually entered daily class times and the local clock; rotating schedules, notifications outside the page, actual file attachments, and dedicated distraction-free task screen are not included. Resource links are supported. Achievements are derived from current saved records and are not independent verification. Reports are student-entered records, not proof of time or submission. 
