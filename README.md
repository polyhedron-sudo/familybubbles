# Family Bubbles v4

A plain HTML/CSS/JavaScript family scrapbook. Open `index.html` in a modern browser. D3 is loaded from jsDelivr, so an internet connection is required unless D3 is bundled locally.

## Storage and backups

Family data is stored in the browser's IndexedDB database, which supports much larger records (including embedded photo data) than localStorage. On first launch, the app attempts to migrate an existing Family Bubbles v2 localStorage save into IndexedDB.

Use **Export Family** to create a portable `.json` backup containing people, relationships, biographies, dates, notes, and embedded image data. Use **Import Family** to restore that backup. Keep exported JSON files somewhere safe; browser storage is local to the browser and device.

The on-screen view focuses on one person and displays relatives within three relationship steps. The underlying data can contain more people and relationships.

## Portrait geometry update (v19)
- Portrait images are clipped to a circle matching each bubble's radius.
- The clickable/drag target is circular and matches the visible bubble rather than the square image bounds.
- Dropping a photo creates a relationship only when the drop point is inside a person's circular bubble.
- Double-clicking a person focuses the bubble and leaves that person's details panel open.

## v21 — Focus-aware relationship controls
- Parent, Partner, Sibling, and Child controls follow the currently focused bubble.
- When focus changes, the previous controls fade away and the new set fades in around the newly centered person.
- Existing family relationships are not changed by changing focus.
