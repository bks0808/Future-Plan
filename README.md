# Life Plan Budget

A single-page planning model for three linked decisions: buying a house, what it costs to
live in it, and paying for a wedding. No build step, no dependencies, no backend — one
self-contained HTML file.

**Live site:** `https://YOUR-USERNAME.github.io/REPO-NAME/`
_(fill this in once Pages is live)_

---

## First-time setup

1. Create a GitHub account at [github.com](https://github.com) if you don't have one.
2. Click **+** (top right) → **New repository**.
   - Name it something like `life-plan`
   - Set it to **Public** (see [Is this safe?](#is-this-safe) below — Pages on a private repo
     requires a paid GitHub Pro plan, and the app itself contains none of your data)
   - Leave every other option alone, click **Create repository**
3. On the empty repo page, click **uploading an existing file**.
4. Drag in both files from this folder: `index.html` and `README.md`.
5. Click **Commit changes**.
6. Go to **Settings** → **Pages** (left sidebar).
7. Under *Build and deployment*, set **Source** to `Deploy from a branch`, **Branch** to
   `main` and folder to `/ (root)`. Click **Save**.
8. Wait about a minute, then refresh. GitHub shows your URL at the top of the Pages settings.

Bookmark that URL on your laptop and your phone. It's the same app, now reachable anywhere.

---

## Updating it later

Open the repo → click `index.html` → click the pencil icon → paste the new version → **Commit
changes**. The live site updates within a minute.

Or drag a replacement `index.html` onto the repo file list and commit. Either works; you never
need to install git or touch a command line.

---

## How sharing works

Click **Share** in the app. Your inputs get packed into a short code appended to the URL after
a `#`. Send the link, and whoever opens it sees exactly your numbers.

Only what you've changed from the defaults is encoded, so a typical link is a few hundred
characters rather than a few thousand.

The address bar keeps itself in sync as you edit, so bookmarking the page bookmarks your
current scenario.

---

## Is this safe?

**The repository is public. Your numbers are not in it.**

`index.html` ships with generic placeholder defaults — a $450,000 house, $170,000 combined
income, a $34,200 wedding. Those are national averages, not yours. Anyone who finds the repo
sees the calculator, not your finances.

**Your data lives only in links you personally create.** Two things follow from that:

- **Good:** the part of a URL after `#` is never transmitted to the server. It's a browser
  convention, not a courtesy — GitHub's servers physically never receive your income, savings
  balance, or debts. No server logs them because no server sees them.
- **Bad:** the code is base64, which is encoding, not encryption. Anyone holding the link can
  decode it in seconds. Treat a share link exactly like a screenshot of your bank statement:
  fine to text your partner, not fine to post in a Slack channel, paste into a public issue,
  or commit to this repo.

Don't put a share link in this README, in a commit message, or anywhere in the repo's history.
Git history is very hard to scrub.

**Don't host this on a work GitHub organization.** Org admins can read private repos.

---

## What's in the app

| Tab | What it does |
|---|---|
| **Dashboard** | The three big numbers, a verdict panel, and stress tests |
| **House** | Price/down-payment/rate sliders, cash to close, PITI breakdown, lender ratios, 30-year amortization |
| **Living Costs** | Editable monthly line items; housing rows calculate themselves |
| **Wedding** | Vendor tracker with estimates, contracted amounts, deposits, and due dates |
| **Timeline** | 60-month cash projection with the house and wedding outflows firing on your target dates |
| **Notes** | Sources, assumptions, and how to use it |

There's also a companion spreadsheet. Put that on Google Sheets when two people need to edit
the same numbers at the same time — two browsers running this app each hold their own copy and
will overwrite each other.

---

## Sources for the defaults

- Mortgage rate 6.66% — [Freddie Mac PMMS](https://www.freddiemac.com/pmms), 30-year fixed
  average, week of 2026-07-30
- Wedding budget $34,200 and 117-guest average — The Knot 2026 Real Weddings Study
  (10,474 US couples married in 2025). The *median* is meaningfully lower than the mean.
- Property tax, insurance, and HOA have no useful national default. Look up your county.

This is a planning model, not financial advice. Confirm every figure with your lender,
insurer, and tax authority before committing to anything.
