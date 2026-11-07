# Ensuite

Ensuite combines flashcards, daily habits, a Pomodoro timer, and a day and week planner in one self-contained HTML workspace. A persistent sidebar switches between all four tools without interrupting your focus timer.

## Getting started

Download `Focus.html` and open it in a modern browser. No installation, account, or server is required. Keep using the same browser profile and file location to access your saved data. When upgrading from an older filename, export your cards, habits, and planner backups first and import them into `Focus.html` if your browser treats the renamed file as a new storage location. On the same origin, existing databases and preferences remain compatible.

## Flashcards

Create named decks and enter one card per line using `front::back`. Both sides support Markdown and mathematical notation. Edit cards, rename decks, or delete either as needed. Use **Export** in a deck's toolbar to download just that deck as a JSON backup, including its cards and review progress. **Study** reviews due cards using spaced repetition, while **Cram** practices every card without changing its review schedule.

## Habits

Add daily habits, mark them complete, and track consecutive-day streaks. Undo today's completion when necessary. Habits can also be renamed or deleted.

## Focus timer

Set work duration, break duration, and cycle count. Start, pause, resume, or reset your session. The timer continues when you switch tools. Focus starts with a plain background. Turn Scene on to display the supplied painting, choose an image or GIF background, use a direct image URL, or restore the original painting. The supplied painting is embedded unchanged and shown at its original color and brightness, with no tint, desaturation, dimming, or blur. The image fills the timer area and may crop to fit the window; compact dark controls provide their own contrast. Ambient recordings include rain, fireplace, river, thunderstorm, crickets, and birds. An optional Spotify player accepts supported Spotify links and remembers your selection after reload.

## Slot

Add tasks with assigned dates, durations, deadlines, and priorities. Slot automatically updates schedules when tasks, deadlines, commitments, or availability change. Day and Week views show the current plan; there is no Generate or Push Tomorrow step.

Use **Edit** or **Delete** on tasks in the day schedule, Week previews, Tasks, Upcoming, or skipped history. The editor includes name, type, date, duration, deadline, priority, energy, single-block preference, chunk limits, and checklist contents/checkmarks. Saving recalculates schedules and keeps your selected date and view. Completed work retains its original times and labels; duration cannot fall below completed minutes, and increasing a completed task's duration reopens it. Deleted tasks go to **Tasks → Trash** and can be restored.

Use **Adjust / keep time** on an unfinished block to change its start time or keep its current placement. Automatic planning reserves that time until you choose **Release time**. If hours, commitments, or a deadline change around it, Slot keeps the placement and flags the conflict. Release kept times before changing that task's assigned date, duration, type, or chunk limits. Completed and skipped records remain in history. Skipped intervals stay clear during automatic retries.

At the start of a new local day, unfinished work rolls into the earliest available periods around assigned work, commitments, and kept times. Remaining chunks can span several days. Original deadlines, completed minutes, and checklist checkmarks stay unchanged. Slot places what fits before the deadline, then schedules excess work in the next feasible periods with a deadline warning. Work without a verified placement remains visible. Rollover checks while the page is open and catches up when reopened or brought into focus; a closed HTML file cannot run in the background. Catch-up searches the next 90 days.

Enable **Repeat task weekly** when adding either task type. Choose weekdays, every day, or individual days—for example, mathematics for 45 minutes every weekday. Each occurrence has its own deadline, time progress, and checklist. **Tasks → Recurring tasks** provides **Edit recurring task**, **Pause**, and **Resume**. Series edits update untouched occurrences from today onward; completed work, checkmarks, individually edited occurrences, deleted instances, and kept times remain intact. Pausing withdraws untouched future instances without deleting history. Resuming starts with today and does not backfill paused days. The app creates a rolling 35-day horizon and also creates the selected future week; reopening extends it without duplicates.

Under **Settings → Weekday availability**, save permanent hours or a day-off rule for selected weekdays. Use multiple windows for split days. **Edit hours** changes a rule and **Reset to default** restores 09:00–17:00. **Usable hours** still saves date-specific overrides, including days off, or seven explicit date overrides. Date overrides take precedence; **Use weekday rule** removes the selected date's override. Every change updates affected schedules.

Turn **Single block** on for an uninterrupted session; it starts off for timed tasks and on for checklist blocks. Slot tries one session first, then the fewest sessions its bounded search can verify. Creation immediately applies the resulting schedule and reports any split. A one-off single-block request without a verified placement is rejected atomically, leaving its draft and saved data intact. Recurring rules can be saved when occurrences cannot fit; those instances stay visible with warnings. With Single block off, manual chunk limits apply. Rollover uses available chunks across days and does not claim a globally minimal multi-day split.

Choose **Checklist block** for to-dos whose individual durations are unknown. Set the block's total duration and enter one item per line. Split sessions of the same occurrence share checkmarks; separate recurring occurrences have independent lists. **Edit** can rename a checklist block or change its items. Item checkmarks and completed time are independent and survive reloads, scheduling changes, rollover, and restoration.

Under **Settings → Fixed commitments**, enable **Repeat weekly** and choose repeat days, **Weekdays**, or **Every day**. Commitments repeat from their Starts date at the same local time and duration, including overnight commitments. **Edit** changes the series; **Delete series** removes it. Changes reschedule unfinished work automatically while protecting completed history and kept times.

## Keyboard shortcuts

Use `Alt+1`, `Alt+2`, `Alt+3`, and `Alt+4` to switch to Flashcards, Habits, Focus, and Slot. During flashcard review in Study or Cram, press Space or use **Show Answer / Show Front** to flip between the front and back as often as needed. With the answer visible, use Left or Right Arrow to grade it.

## Saving and backups

Flashcards, habits, and Slot save in your browser. Export JSON backups regularly, especially before moving devices, clearing browser storage, or importing data. Each tool uses its own compatible backup format. Importing replaces that tool's current data. Slot's backup controls are under **Settings → Backups & storage**.

Slot backups include task recurrence rules and occurrence history, permanent weekday availability, date overrides, kept times, rollover metadata, single-block preferences, checklists, and recurring commitments. Slot backups are interchangeable between the standalone planner and the Ensuite workspace. Older backups still load with no task recurrences or weekday rules; timed tasks keep their chunk settings, and checklist blocks default to a single-session preference.

## Offline use

The core tools, fonts, Markdown renderer, and math support are embedded. Spotify, streamed ambient sounds, and remote background URLs require internet. Focus timer settings, custom backgrounds, and ambient selections last for the current page session and reset after reloading. Spotify links persist unless you clear the player or turn off **Remember my Spotify link**.

## Hidden flashcards

Use **Hide** between **Cram** and **Add Cards** to check cards to exclude from Study, Cram, and spaced repetition, press **Enter** to finish, and restore cards individually by unchecking them in Hide mode or all at once with **Unhide All**.

## Appearance

Ensuite uses a quiet, grayscale interface with black surfaces, neutral text, thin straight rules, and embedded IBM Plex Mono. Open layouts, simple buttons and inputs, and consistent empty states give each tool the same restrained visual language. The timer starts with a plain background; the original painting remains available through the Scene control.

The workspace fills the browser window with square edges, no outer frame or redundant app-name header, and a dark 64-pixel navigation rail (56 pixels on small screens). A slim edge marker and brighter icon identify the active tool. Hover a tool icon for its label and shortcut; keyboard navigation remains available. Decks, forms, and planner blocks adapt to narrow screens, keyboard focus remains visible, and reduced-motion preferences are respected.

## Validation

Open `Focus.html` in a modern browser. Check all four tabs and `Alt+1` through `Alt+4`; create and review a flashcard, complete a habit, add a planner task, and start/pause/reset the focus timer. Check a narrow window and reload to verify saved data. In Focus settings, upload an image, restore the original painting, and switch Scene off/on.

## Font license

IBM Plex Mono is bundled under the SIL Open Font License 1.1. Its full notice is included in `FONT-LICENSE.txt` and inside the self-contained HTML file.
