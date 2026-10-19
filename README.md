# Family Bubbles — v34

Family Bubbles is a plain HTML, CSS and JavaScript genealogy scrapbook, hosted as static files on GitHub Pages. D3.js is loaded from jsDelivr; an internet connection is needed unless D3 is provided locally.

## Navigating the family

- Click or tap a person once to select and highlight them. The selected person's ID becomes the focus for bubble sizing and relationship distance; the view and information panel do not move or open on this first click.
- Click or tap that same person a second time to centre the view on their bubble and open the information panel. There is no special double-click gesture or timing requirement.
- Click or tap another person to select them instead, closing the previous information panel.
- Drag bubbles to move them. Changing focus does not change saved bubble coordinates or family relationships.
- The currently selected person is displayed at 125% of the normal bubble radius (76 vs 61 pixels). Everyone within three relationship links is the same normal size. More distant or disconnected people display at half the normal radius.
- “You” is only the initial demo person's name. Rename it freely: it is not a privileged record.
- The former Parent/Partner/Child/Sibling canvas buttons (PPCS) are disabled.

## Editing and relationships

- The information panel edits a person's name, portrait, dates, biography and notes. Choose **Save Changes** to store edits.
- **Create Person** (green, above Save Changes) opens an inline form to name a new person and optionally connect them as a parent, partner, child or sibling of the person shown in the panel. The new person appears as a bubble; existing positions are retained.
- In **Relationship links**, choose another existing person and a relationship type to create a connection.
- **Delete Person** removes that person and their relationships.
- The app still includes photo drop handling; its behaviour is under review and is not the focus of this release.

## Storage and backups

Family information is stored in the browser's IndexedDB (with a localStorage fallback). Use **Export Family** to save a portable JSON backup containing people, relationships, notes and embedded images. Use **Import Family** to restore a backup. Browser storage is local to each browser/device, so export backups regularly.

## Testing status

v34 adds the Create Person panel action while retaining the working v33 navigation and sizing. JavaScript syntax and archive integrity are checked; visual interaction still requires a browser test.
