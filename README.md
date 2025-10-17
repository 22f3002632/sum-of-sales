# Overview
This single-page app loads Bootstrap 5 from jsDelivr, fetches the bundled data.csv file, sums its "sales" column, sets the page title to "Sales Summary ${seed}", and displays the computed total in the element with id "total-sales".

Key features:
- Title dynamically set to include the provided seed (from window.seed or URL ?seed=).
- Robust CSV parsing with support for quoted fields and commas inside quotes.
- Numeric extraction tolerant of currency symbols and thousands separators.
- Clean UI using Bootstrap 5.

# Setup
1. Ensure data.csv is in the same directory as index.html.
2. Serve the files over a local web server (recommended). Examples:
   - Python: python -m http.server 8000
   - Node (serve): npx serve .
   - PHP: php -S localhost:8000
3. Open http://localhost:8000 in your browser.

Note: Opening index.html directly via the file:// protocol may prevent fetch() from loading data.csv due to browser security restrictions.

# Usage
- Open the app in a browser; it will automatically fetch data.csv and display the sum of the "sales" column inside the "Total Sales" field.
- The title will be "Sales Summary ${seed}". To provide a seed if one isn’t injected into window.seed by your environment, you can pass it via the URL:
  - Example: http://localhost:8000/?seed=12345

No further interaction is required; the page will show the total and a brief load status.