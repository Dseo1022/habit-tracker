# Habit Tracker

A simple habit tracker in a single web page, written in plain HTML, CSS, and JavaScript with no build step or dependencies.

## Features

- **Add habits** by typing a name and pressing Enter or clicking **Add**.
- **Check off today** by tapping the circle next to a habit.
- **Fill in the past week** using the row of day buttons under each habit.
- **Streaks**: the 🔥 count shows how many days in a row a habit has been done. If today isn't checked yet, yesterday's streak still counts, so it only resets after a full missed day.
- **Delete** a habit by tapping **×**, then **Delete?** to confirm.
- **Light and dark mode** follow your system setting.
- **Works on phones**: the layout fits small screens.

## Running it

Open `habit-tracker.html` in any browser. You can double-click it, or drag it into a browser window. There's nothing to install.

## Where your data is saved

The page saves habits in one of two places, and the line under the date tells you which:

| How the page is opened | Where habits are saved | Shown as |
| --- | --- | --- |
| As a local file | This browser's `localStorage`, on this device only | "Saved in this browser only." |
| As a published Claude artifact | Your private space in the artifact's database, synced across every device signed in to the same Claude account | "Synced to your Claude account." |

When the synced version first opens on a device that already has habits in its browser storage, it copies them up, as long as your account has no habits saved yet.

In the synced version, each habit is one document in the viewer's private `data/users/<id>` collection. Nobody else can read these documents, including anyone the page is shared with.

## Files

- `habit-tracker.html`: the whole app, including styles and script.
