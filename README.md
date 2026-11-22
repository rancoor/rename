# Product Naming Standard — Vercel-ready static site

## Deploy to Vercel
1. Extract this ZIP.
2. In Vercel, choose **Add New → Project → Import** and import the extracted folder from a Git repository, or use the Vercel CLI from this folder.
3. Framework preset: **Other**.
4. Build command: leave blank.
5. Output directory: `.` (project root).
6. Deploy.

No build step, API key, database, or server is required. The website is static and loads `public/dictionary.json` in the browser.

## Files
- `index.html` — interactive dictionary, filters and live suggestions.
- `dictionary.json` — merged dictionary records from the reviewed master dictionary and latest edited naming workbook.
- `public/dictionary.json` — browser-served copy of the dictionary.
- `public/Product_Naming_Standardisation_Manual.pdf (v2 rules clarified)` — PDF manual.
- `vercel.json` — static hosting configuration.

## Similarity engine
The browser code combines edit distance (including adjacent-character transposition), token-prefix matching, substring matching and Soundex phonetic matching. Results are recommendations only; they do not edit product names or automatically apply mappings.

## Governance
The dictionary retains category, observed term, approved term, status, mapping indicator, occurrences, applicable item groups, examples, reviewer comments and source. Confirm status and scope before using a suggestion.
