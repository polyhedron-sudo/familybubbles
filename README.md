# Family Bubbles

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

## Current photo workflow

- **Add Photos** accepts one or more images. The newest becomes the main portrait, and previous photographic portraits stay in the album. Photos save automatically when added.
- Up to eight album photos appear as smaller circular bubbles around each person. The person's name now sits below the lowest visible photo bubble with extra spacing, adjusting to bubble size and photo count.
- Expand **Photographs** at the bottom of the panel for thumbnails of the current portrait and every album photo, including photos beyond the eight surrounding bubbles.
- Select a thumbnail or surrounding photo bubble to open that photo full-screen. Use left/right buttons or arrow keys to browse, wrapping at either end. Close with **×** or **Escape**.
- Supported raster uploads and imported photos are optimized to a maximum of 960 pixels on the longest side and converted to JPEG with a white background. Image bytes may therefore change during import.

## Help and reset

Use the **?** button next to **Reset** in the top toolbar for the full instructions. The **Reset** button is the same function previously labeled “Reset Demo”: it restores the demo family after confirmation, replacing the current family stored in this browser. Export a backup first.

## Storage and backups

Family information is stored in the browser's IndexedDB (with a localStorage fallback). Use **Export Family** to save a portable JSON backup containing people, relationships, notes and embedded images. Use **Import Family** to restore a backup, replacing the family currently stored in this browser. Exports include main portraits and complete albums, including photographs beyond the eight surrounding bubbles. Import does not merge families. Browser storage is local to each browser/device, so export backups regularly.

## Testing status

The user reports that the photo workflow works well. The latest name-spacing fix has passed JavaScript syntax and geometry checks for all three bubble sizes and zero through ten album photos, including the eight-satellite limit. Its visual appearance still needs a browser check. Earlier release packages had JavaScript syntax and archive integrity checks.

## Latest update — Name spacing

Names sit below the lowest visible surrounding photo bubble rather than just below the main portrait. People without surrounding photographs keep their previous label position.

## v39 — Photograph optimization

Raster uploads and imported photographs are optimized to a maximum of 960 pixels on the longest side for smaller backups and more responsive viewing.


## v37 — Additional photograph bubbles
This release introduced **Add Photos** and album photographs around each person. The v38 behavior below supersedes its original portrait-handling behavior. Up to eight additional images appear around the person's bubble at half its diameter. Every attached photograph is accessible from the thumbnail gallery in the side panel; select a thumbnail or satellite to enlarge it. Additional photos are embedded in JSON exports. This version does not merge JSON files or split the original portrait.

## v38 photo viewer

New image uploads become the main portrait, with previous photographic portraits retained in the person’s album. The Photographs section at the bottom of the side panel is collapsed by default and contains thumbnails of the current portrait and all older photographs. Click a thumbnail or surrounding photo bubble for a full-screen viewer; use left/right buttons or arrow keys to browse and X or Escape to close. All embedded images remain in JSON exports.
