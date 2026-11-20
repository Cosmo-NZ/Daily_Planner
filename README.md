# Daily Planner Generator

A single HTML page that builds a personalised, fully hyperlinked PDF daily planner for e-ink tablets such as Boox.

Everything runs in your browser: no install, no account, and nothing is uploaded anywhere.

## Using it

1. Open `daily-planner-generator.html` in any modern browser, either straight from disk or from any static web host.
2. Choose your settings. The preview on the right updates as you go.
3. Click **Generate PDF**. A full year takes a few seconds, and the PDF downloads when it's done.
4. Copy the PDF to your tablet and open it in a reader that supports internal links.

## Settings

| Setting | Options |
|---|---|
| Document name | Shown on the cover and used in the file name |
| Calendar year | 2026 to 2035 |
| Week start | Monday or Sunday |
| Handedness | Right or left (left mirrors the navigation to the other side) |
| Planner font | PT Sans (default), Inter, Atkinson Hyperlegible, Bitter, PT Serif |
| Schedule from / to | 06:00 to 20:00 in 30-minute steps (default 08:30 to 17:00) |
| Interval | 30 or 60 minutes per schedule row |
| Daily notes pages | 1, 2 or 3 per day |
| Cover page | On or off |

## What's in the PDF

- **Cover** (optional): the planner name and year, with a grid of the 12 months.
- **Month calendar page**, just before each month's 1st: a date grid where every date links to its day, plus a notes area.
- **Daily Plan page** for every day: tasks with checkboxes, a reminders box, and a timed schedule.
- **Daily Notes pages** (1 to 3 per day): lined pages for writing.

Pages are 540 × 720 pt (7.5 × 10 in, a 3:4 ratio) to match tablet screens. They aren't sized for printing on paper.

### Navigation

- **Month tabs** at the top of every page open that month's calendar page.
- **Day buttons** under each day's title jump to the other days of that week.
- **◀ ▶ arrows** step a week on day pages and a month on calendar pages.
- **Daily Plan ⇄ Daily Notes** buttons switch between a day's pages, and numbered tabs pick a notes page.

With the default settings a 2026 planner is 1,108 pages.

## Offline use

The page works without an internet connection:

- **Fonts** are built into the file (latin character set only).
- **PDF engine:** the page loads jsPDF 4.2.1 from jsDelivr and falls back to an identical copy built into the file if it can't reach the internet.

## Credits

- [jsPDF](https://github.com/parallax/jsPDF) (MIT licence)
- Fonts, all under the SIL Open Font License 1.1:
  - PT Sans and PT Serif by ParaType
  - Inter by Rasmus Andersson
  - Atkinson Hyperlegible by the Braille Institute
  - Bitter by Huerta Tipográfica
