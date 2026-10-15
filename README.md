# Family Bubbles v4

A plain HTML/CSS/JavaScript family scrapbook. Open `index.html` in a modern browser. D3 is loaded from jsDelivr, so an internet connection is required unless D3 is bundled locally.

## Storage and backups

Family data is stored in the browser's IndexedDB database, which supports much larger records (including embedded photo data) than localStorage. On first launch, the app attempts to migrate an existing Family Bubbles v2 localStorage save into IndexedDB.

Use **Export Family** to create a portable `.json` backup containing people, relationships, biographies, dates, notes, and embedded image data. Use **Import Family** to restore that backup. Keep exported JSON files somewhere safe; browser storage is local to the browser and device.

The on-screen view focuses on one person and displays relatives within three relationship steps. The underlying data can contain more people and relationships.


Version 17 update: corrected family-bubble portrait rendering. Portrait images are clipped to a circle, and the circular border is transparent in the middle so it cannot cover the photo. This iteration uses Family-Bubbles-fixed-v11 as its starting foundation.
