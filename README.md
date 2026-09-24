# Oshawa Claims Dashboard

## Publish on GitHub Pages

1. Extract Claims-Dashboard-GitHub.zip.
2. Upload all extracted files and the assets folder to the root of your Claims-Dashboard repository. Do not upload the ZIP itself or put everything inside another folder.
3. Commit the files.
4. Go to Settings > Pages. Choose Deploy from a branch, main, /(root), then Save.
5. Open the website link shown by GitHub when deployment completes.

## Update claims

1. Open the published dashboard and reload it to get the latest published data.
2. Click Prepare Excel update and select the complete annual Excel workbook.
3. Check the register year. A filename such as 2027 Claims Track.xlsx sets it automatically; you can correct it.
4. Check the preview and click Preview & download claims.json.
5. In the GitHub repository, choose Add file > Upload files and upload the downloaded claims.json, keeping that exact filename. Commit changes.
6. Wait for GitHub Pages to finish publishing, then reload the dashboard.

Selecting Excel and downloading data changes only your preview. Other visitors see the update after claims.json is committed and published. Each download contains every register, replacing only the selected year. Coordinate publishing with colleagues to avoid overwriting a newer update. People uploading to GitHub need repository write access.

## Annual workbooks

Use a separate workbook each year, with the same headings as the supplied 2026 workbook. The importer reads the first worksheet containing Type of Loss and Loss Location. Required headings: Date, Type of Loss, Loss Location, Date of Loss, x, y. Optional: Response Status, Response Date. Use real Excel date cells. x is latitude; y is longitude. Blank coordinates are allowed; those claims remain in the table and totals.

2027 and later registers are added automatically when their data is published. Earlier loss dates stay in the selected register and can be filtered using Loss before [year].

## Data and privacy

Initial data includes 53 claims from the supplied 2025 workbook and 50 from the updated 2026 workbook. Claimant names, staff names and notes are excluded. Excel is read locally in the browser and is not uploaded by this website. Do not commit original Excel trackers to this public repository. All committed website data, including location, dates and status, is public.

The 2025 register contains 53 claims: 51 responded and 2 in progress. There are 46 losses in 2025 and 7 earlier losses. Two claims lack coordinates and remain in totals and the table. The received-date typo 03/019/2025 was normalized to March 19, 2025. Loss dates are unchanged.

## Dependencies

Built with React, Leaflet, Leaflet.markercluster, SheetJS, Radix UI, Lucide and Tailwind CSS. Street tiles are supplied by OpenStreetMap and satellite tiles by Esri. Map imagery requires internet access. The ZIP contains compiled browser assets and needs no build step or ChatGPT login.
