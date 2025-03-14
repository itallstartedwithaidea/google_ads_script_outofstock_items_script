# Website Out-of-Stock Scanner

This Google Apps Script scans specified website pages to identify out-of-stock items and logs the results into a Google Sheet for easy monitoring and management.

---

## Features

- **Automated Website Scanning:** Regularly checks specified webpages for out-of-stock items.
- **Real-Time Updates:** Updates a Google Sheet with the latest out-of-stock information.
- **Hourly Monitoring:** Set up to automatically run every hour.

---

## Installation

Follow these simple steps to install and use the script:

### 1. Set Up Google Sheet
- Create a new Google Sheet.
- Add a new sheet named `OutOfStock`.
- Note the Sheet ID from the URL (e.g., `https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID/edit`).

### 2. Open Google Apps Script
- Open your Google Sheet.
- Navigate to **Extensions → Apps Script**.

### 3. Create the Script
- Delete any default code.
- Paste the provided `scanWebsiteForOutOfStockItems` script.

### 4. Configure the Script
Update the following lines:

```javascript
const urls = ['https://yourwebsite.com/page1', 'https://yourwebsite.com/page2']; // Add URLs to scan

const sheet = SpreadsheetApp.openById('YOUR_SHEET_ID').getSheetByName('OutOfStock');
```

Replace:
- `'https://yourwebsite.com/page1'` and `'https://yourwebsite.com/page2'` with your actual website URLs.
- `'YOUR_SHEET_ID'` with your actual Google Sheet ID.

### 5. Install Cheerio Library
- In Apps Script, click on **Libraries** (left menu, icon looks like a puzzle).
- Add Cheerio Library using Script ID: `1Ree69m13ntLYAfq-9I0mviq01D3bO9qkikUO06n89F5iBSf97j-GPC5K`.

### 6. Save and Authorize
- Click the **Save** button.
- Run the script once manually (`scanWebsiteForOutOfStockItems`) to authorize permissions.

### 7. Set Up Hourly Trigger
- Run the provided function `createHourlyTrigger()` once to automatically set up hourly checks.

---

## Usage

- The Google Sheet named `OutOfStock` will be updated hourly, listing all currently out-of-stock items and their respective page URLs.
- Monitor this sheet to manage inventory and update your online store accordingly.

---

## Troubleshooting

- Ensure URLs are correct and accessible.
- Verify your website's HTML structure matches the selectors used in the script (e.g., `.out-of-stock`, `.item-name`). Update selectors if necessary.

---

## Support

For assistance or customization, please contact your developer or technical support.

