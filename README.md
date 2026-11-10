# Must Go: Vermont

A single-page map and table of the Vermont businesses r/vermont says are worth driving out of your way for.

It is built from the Reddit thread **"What Vermont business is actually worth driving out of your way for?"** Every business named in the comments is listed with how many upvotes backed it, what kind of place it is, and where it is.

**Live site:** https://skidude89.github.io/mustgovermont/ (once GitHub Pages is enabled for this repo)

## What you get

- **A table of 198 businesses**, ranked by upvotes. Each row has the business type, the town, the upvote total, how many comments mentioned it, and a link to its Google Maps listing.
- **A map of Vermont** with a pin for each of the 189 businesses that could be placed. Pin size shows upvotes and pin color shows business type. Click a pin or a table row for details and the Maps link.
- **Search and filters:** search by business or town, filter by type (pizza, brewery, creemee, bookstore and so on), and sort by name, type or upvotes.
- **9 businesses with no pin,** because the comment gave only a name and I couldn't place them. They still appear in the table.

## How to use it

It is one self-contained file, `index.html`. There is nothing to install or build.

- **Online:** turn on GitHub Pages (Settings, then Pages, source `main`, folder `/ (root)`) and open the link above.
- **On your computer:** open `index.html` in a browser. If the street map doesn't load, serve it locally instead: run `python3 -m http.server 8000` in this folder and open http://localhost:8000.

Street-level map tiles come from OpenStreetMap and need an internet connection. The Vermont outline and county lines are built into the file, so pins show even when the tiles don't load.

## How the numbers were made

- **Upvotes** are the sum of the scores of the comments that name a business or clearly endorse it. That includes direct replies like "100% agree" or "so good." A comment naming several places counts in full for each one.
- Criticism, jokes, and comments with a score of 0 or below add nothing.
- The data comes from a saved copy of the thread with all replies expanded: 387 comments were readable (Reddit listed 397).
- Endorsing replies were matched by a keyword rule plus a manual pass, so a point or two on some rows may be off.
- **Left out:** state parks (not a business), closed places, Pizza Man (only lukewarm replies), and generic replies.

## Things to know

- **Pins are approximate,** at town or village level, not the storefront. Most locations came from my own knowledge plus web searches, and a few are guesses (for example April's Maple and Red Onion). The Google Maps links search by name and town and are the reliable way to find the real spot.
- Hick's Orchard is just across the line in Granville, New York.
- Businesses move and close. Red Hen Baking, for one, was reported to have moved to Main Street in Montpelier. Check hours before you drive.

## Built with

Plain HTML, CSS and JavaScript, with [Leaflet](https://leafletjs.com) (inlined) for the map, [OpenStreetMap](https://www.openstreetmap.org/copyright) tiles, and state and county outlines from [US Atlas](https://github.com/topojson/us-atlas).
