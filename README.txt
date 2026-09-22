ARIVE Homes Build Milestone Dashboard - redesigned to match the approved mockup.

FILES
- index.html: complete GitHub Pages dashboard (single-file deployment)

DATA CONNECTION
- Uses the existing Apps Script web app URL already configured for the Homes tab.
- Expected headers: Home / lot, Community, Plan, Superintendent, Home type, Dig date, 4-way actual, Cabinets actual, C/O actual, Notes.
- Apps Script may return {ok:true, version, headers, rows, fetchedAt}; arrays are mapped to objects using headers.
- Uses JSONP so the GitHub Pages site can read the Apps Script endpoint without requiring a server.

TARGETS
- Single Family: 4-Way 63 days, Cabinets 111 days, C/O 150 days from Dig.
- Townhome: 4-Way 100 days, Cabinets 160 days, C/O 205 days from Dig.

BEHAVIOR
- Default Active homes exclude homes with a C/O actual date.
- Completed and All Homes retain closed homes.
- Dig is always visible.
- 4-Way, Cabinets, and C/O can be hidden from Settings.
- Visibility is stored in the URL hash and carries into shared links, printed views, tables, deadlines, and CSV export.
- This Week includes overdue, due this week, and next week.
- Scorecard supports all supers or an individual super.
