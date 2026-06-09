# Find Your Seat — guest lookup site

A single-page website for guests to look up their table on the wedding day.
Guests scan a QR code, type their name, and see their table number, who they're
sitting with, and where the table is in the room. Works on any phone.

## What's in this folder

- `index.html` — the website (search, fuzzy "did you mean", tablemates, room map).
- `seating-data.js` — the only file that changes. It holds each table's number and who sits there.

## Preview it now

Double-click `index.html`. It opens in your browser with the current arrangement. Try typing a name.

## Update it when the seating changes (easy, no code)

1. In the seating builder, finish your changes.
2. Click the **Save site data** button. It downloads a fresh `seating-data.js`.
3. Replace the old `seating-data.js` in this folder (or in your GitHub repo) with the new one.

That's the whole loop. `index.html` never needs to change — the map, search, and
numbering all read from `seating-data.js`.

## Host it free on GitHub Pages

1. Make a free account at github.com (if you don't have one).
2. Create a new **public** repository, e.g. `find-your-seat`.
3. On the repo page: **Add file → Upload files** → drag in `index.html` and `seating-data.js` → **Commit**.
4. **Settings → Pages →** under "Build and deployment", Source = "Deploy from a branch",
   Branch = `main`, folder = `/ (root)` → **Save**.
5. Wait ~1 minute. Your live URL appears at the top of the Pages settings:
   `https://YOUR-USERNAME.github.io/find-your-seat/`

To update later: upload the new `seating-data.js` to the repo (Add file → Upload files,
same name, commit). The site refreshes within a minute.

## QR code

Once you have the live URL, make a QR code that points to it (any free generator works,
e.g. qr-code-generator.com). Print it in your frames around the venue. Tell Claude the
final URL and it can generate the QR image for you.

## Notes

- Only guests who are seated appear in search. Deploy the final version once everyone is assigned.
- The site shows full names of tablemates (normal for a seating display). No emails, phones, or dietary info are exposed.
