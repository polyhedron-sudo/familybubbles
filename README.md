# Family Bubbles — v36

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

**Refresh View:** If a new portrait or relationship line does not appear immediately, click **↻ Refresh View** below Delete Person in the information panel. The page reloads to display saved changes. Save any unsaved edits first.

## Help and reset

Use the **?** button next to **Reset** in the top toolbar for the full instructions. The **Reset** button is the same function previously labeled “Reset Demo”: it restores the demo family after confirmation, replacing the current family stored in this browser. Export a backup first.

## Storage and backups

Family information is stored in the browser's IndexedDB (with a localStorage fallback). Use **Export Family** to save a portable JSON backup containing people, relationships, notes and embedded images. Use **Import Family** to restore a backup. Browser storage is local to each browser/device, so export backups regularly.

## Testing status

v36 renames Reset Demo to Reset and adds an instructions panel. v35 adds the information-panel Refresh View button to v34; v34 adds the Create Person panel action while retaining the working v33 navigation and sizing. JavaScript syntax and archive integrity are checked; visual interaction still requires a browser test.


## v37 — Additional photograph bubbles
Open a person's panel and use **Add Photos** to attach one or more images without changing the original portrait. Up to eight additional images appear around the person's bubble at half its diameter. Every attached photograph is accessible from the thumbnail gallery in the side panel; select a thumbnail or satellite to enlarge it. Additional photos are embedded in JSON exports. This version does not merge JSON files or split the original portrait.

## v38 photo viewer

New image uploads become the main portrait, with previous photographic portraits retained in the person’s album. The Photographs section at the bottom of the side panel is collapsed by default and contains thumbnails of the current portrait and all older photographs. Click a thumbnail or surrounding photo bubble for a full-screen viewer; use left/right buttons or arrow keys to browse and X or Escape to close. All embedded images remain in JSON exports.
