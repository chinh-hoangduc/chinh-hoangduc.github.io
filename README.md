# Personal site — Chinh Hoang-Duc

Lives at https://chinh-hoangduc.github.io

Pure HTML + CSS. No build step. Edit `index.html`, push, done.

## Common edits

All edits below are made in `index.html`. Find the section by its `<!-- ============== ... ============== -->` banner.

### Add an abstract to a paper

Find the paper, look for:

```html
<details>
  <summary>Abstract</summary>
  <p class="abstract-placeholder">Abstract coming soon.</p>
</details>
```

Replace with:

```html
<details>
  <summary>Abstract</summary>
  <p>Your abstract text here. Plain English, one or two paragraphs.</p>
</details>
```

(Remove the `class="abstract-placeholder"` so it isn't shown in muted italic.)

### Add a new working paper

In the **Working Papers** section, copy an existing `<article class="paper">…</article>` block and edit the title, status, and PDF link.

### Add a new publication

In the **Publications → Peer-reviewed articles** list, copy any `<li>…</li>` and edit:
- author list (use `<span class="me">Hoang-Duc, C.</span>` to bold your own name)
- year
- title (wrap with `<a href="…">…</a>` pointing to the DOI or journal page)
- journal name in `<em>…</em>`

### Replace journal homepage links with specific DOIs

Each published-paper link currently points to the journal homepage. To swap for the article DOI, just change the `href`.

### Update CV

Replace `Chinh_Hoang-Duc_Resume.pdf` with your new PDF (keep the same filename) and the CV link still works. If you change the filename, also update the link in the header section of `index.html`.

### Change the photo

Replace `photo.jpg`. Keep the filename, or update `<img src="photo.jpg" …>` in the header.

### Change the accent color

Open `style.css`. Top of file:

```css
:root {
  --accent: #7a1f2b;   /* burgundy — change this hex */
  --accent-soft: #a44352;
}
```

A few alternative academic palettes you can paste in:
- Oxford blue:  `--accent: #14213d; --accent-soft: #415a77;`
- Forest green: `--accent: #2d5016; --accent-soft: #6a8e3f;`
- Teal:         `--accent: #1f5d6c; --accent-soft: #4a8a99;`

## Editing workflow

Three options, pick whichever suits the moment:

1. **In your browser, on github.com** — click `index.html`, click the pencil icon, edit, click "Commit changes". Live in ~30 seconds.
2. **Locally in VS Code** — edit, then in the terminal:
   ```
   git add .
   git commit -m "update bio"
   git push
   ```
3. **Ask Claude Code** — open this folder in Claude Code and say "add this paper" or "update bio".

## Items still to fill in

Search `index.html` for `TODO` — they mark:
- Google Scholar profile URL
- GitHub profile URL (or delete that link if you don't want one)

## Local preview

Just open `index.html` in your browser. No server needed.
