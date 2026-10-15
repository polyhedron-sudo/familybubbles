# Family Bubbles v15

A plain HTML/CSS/JavaScript family scrapbook based on the v11 source. Open `index.html` in a modern browser. D3 and JSZip load from jsDelivr, so an internet connection is required unless those libraries are bundled locally.

## Family data and sharing

Family data is stored in browser IndexedDB. Choose **Export Family** to create `familybubble-save.zip`, containing the family JSON and embedded compressed photos, including contributor credits and Recently Deleted items. Import the ZIP directly in the app; older `.json` family exports remain supported. ZIP import replaces the family currently stored in that browser after confirmation.

Photos are resized to a maximum dimension of 480 pixels and converted to JPEG before they are saved. Full-resolution originals are not retained. Replaced main photos are moved into the person's additional-photo collection. Each photo can carry an optional contributor credit. Deleted people, their relationship records, and deleted album photos are retained in Recently Deleted until permanently removed.

The map focuses on one person and displays relatives within three relationship steps; the underlying family remains unlimited. Relationship lines share a consistent dotted style.
