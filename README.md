# BibTeX Generator

This is a small browser-based tool for generating BibTeX entries (`.bib`) without installing anything or using external services.

You fill in a form, click **Generate**, and get a valid BibTeX entry you can copy, download, or save locally in your browser.

No backend. No tracking. No libraries beyond Bootstrap for layout.


## Why?

Decided to vibecode this because while writing my thesis wanted something like this to exist. 


## How it works

- The UI is a simple HTML form styled with **Bootstrap + Bootswatch**
- All logic runs in plain JavaScript
- Generated BibTeX is shown in the output box
- Saved entries are stored using **Local Storage**
- Nothing is sent over the network

If you reload the page:
- the form is cleared
- saved entries are loaded back automatically


## Citation keys

- You can enter a citation key manually
- If you leave it empty, one is generated automatically from:
  - author
  - year
  - title

Example: redhat-2025-infrastructure


## Required fields

Each entry type has required fields (for example `author`, `title`, `year`).

If you leave a required field empty:
- a reasonable default value is used
- generation never fails just because a field is missing

You can always edit the generated BibTeX manually afterwards.


## Saving entries

- Click **Save** to store the current entry in your browser
- Saved entries appear on the right
- Each saved entry can be:
  - copied
  - downloaded as a `.bib` file
  - loaded back into the editor
  - deleted

You can also download **all saved entries** as one `.bib` file.


## Tech notes

- Plain HTML + JavaScript
- Bootstrap 5 + Bootswatch for layout
- Local Storage for persistence
- No build step
- No dependencies beyond CDN CSS

This is meant to stay simple and easy to modify.


## License

Do whatever you want with it. It is vibecoded :D