# Logo Design Portfolio

Static portfolio site for GitHub Pages. No build step needed.

## Folder structure

```
your-repo/
├── index.html
└── images/
    ├── Cream B Logo with Green Arrow.png
    ├── 10.png
    └── ... (all your logo files from Drive)
```

## Deploy on GitHub Pages

1. Download your Drive folder (right-click folder > Download). Unzip it.
2. Create a GitHub repo named `YOUR-USERNAME.github.io` (for the URL `https://YOUR-USERNAME.github.io`).
3. Upload `index.html` to the repo root.
4. Create an `images` folder in the repo and upload all the logo files into it, keeping the original filenames.
5. Go to **Settings > Pages**, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and Save.
6. Wait 1-2 minutes. Your site will be live.

## Customise

Open `index.html` and edit the `CONFIG` and `WORKS` blocks near the bottom:

- `CONFIG`: your name, email and social links.
- `WORKS`: change each logo's `title` and `tag`, reorder, or add new logos.

To add a new logo, upload it to `images/` and add a line:

```js
{ file:"my-logo.png", id:"", title:"My Logo", tag:"Logo" },
```

## Brand kits (GrowthFlux and Bizonomy)

The **Brand Kits** section has exactly two cards: **GrowthFlux** and **Bizonomy**. Each shows the palette (click a swatch to copy its hex), fonts, deliverables, and a **View brand kit** button that opens the PDF from your Google Drive inside the site.

- The PDFs are about 20 MB each, so they stay on Google Drive. In Drive, share each PDF as **Anyone with the link can view**, otherwise visitors will be asked to sign in.
- The hex codes (Obsidian, Ivory, Sage green) are approximate. Replace them in the `BRANDS` list with the exact values from each kit.
- Optional: export a few pages of each PDF as images, save them in `images/brands/` (for example `growthflux-01.jpg`) and list them under `images:` for that brand. The site then shows an image gallery with a full-screen viewer.

## About section: charcoal artwork + Instagram

The About section has two portrait frames next to your name and intro, plus **The Charcoal Wall**, a gallery of up to 6 more works, followed by a bold **Follow on Instagram** banner linking to https://www.instagram.com/artistic_pavan_/ (the link is also in the Contact section and at the end of About).

### Add your charcoal works

Save your scans or photos in the `images/art/` folder with these names (portrait-shaped images work best):

| File | Where it appears |
|---|---|
| `portrait-01.jpg` | Large frame beside your name |
| `portrait-02.jpg` | Small frame beside the intro |
| `portrait-03.jpg` to `portrait-08.jpg` | The Charcoal Wall gallery |

- Empty gallery slots hide automatically as soon as you add at least one work in the gallery.
- Clicking any work opens a full-screen viewer; visitors can flip through all your works.
- To rename files or edit captions, change the `ART` list inside the About script near the bottom of `index.html`.

### Add your charcoal videos (3 slots)

Under the picture gallery there is an **In motion** section with three video frames. Save your clips in a new folder `images/videos/`:

| File | Where it appears |
|---|---|
| `video-01.mp4` | First video frame |
| `video-02.mp4` | Second video frame |
| `video-03.mp4` | Third video frame |

- On desktop the clip previews (muted) when you hover the frame, and clicking opens a full-screen player with sound. On phones, tapping opens the player.
- Use MP4 (H.264). Keep each file under 25 MB so it uploads through the GitHub website. Shrink large clips for free with HandBrake (handbrake.fr) or an online compressor.
- Portrait (reel-style) clips work. To fit a different shape, change `ar: "4/5"` in the `VIDEOS` list in `index.html` (for example `"9/16"` or `"16/9"`).
- To use a different filename, or add a cover image (`poster: "cover-01.jpg"` saved in `images/videos/`), edit the `VIDEOS` list in the About script.
- Empty video slots hide automatically once you add at least one video.

### Getting your work from Instagram onto the site

Instagram does not allow other tools to copy images from a profile, so there are two ways:

1. **Show your real posts live (easiest):** on instagram.com open a post, tap the three dots, choose **Copy link**. Paste the links into the `INSTAGRAM_POSTS` list in the About script (the comment above it shows the format). Those posts then appear as Instagram embeds under the follow banner, always up to date. Only posts from a public account can be embedded.
2. **Add the images themselves:** use the original files from your phone or computer (scans, camera roll). If you only have them on Instagram, request them via Instagram > Settings > Accounts Center > Your information and activity > Download your information, then pick the best ones and save them as `portrait-XX.jpg`.

## Add your UI/UX projects

The site has a **Web Projects** section for your UI/UX and web design work. In `index.html`, find the `WEB` list and replace the 3 sample entries with your own:

```js
{ title:"My Cafe Website", desc:"Responsive site for a local cafe with an online menu.",
  tech:["HTML","CSS","JavaScript"],
  live:"https://my-cafe.example.com",
  code:"https://github.com/YOUR-USERNAME/cafe-site",
  image:"cafe.png",      // screenshot saved in images/web/cafe.png
  color:"#2F6B4F" },
```

- Take a full-page screenshot of each site and put it in `images/web/`.
- Leave `live` or `code` as `""` to hide that button.
- Add as many projects as you like; the grid adjusts automatically.

## Notes

- If a local image is missing, the site tries to load it from your Google Drive link as a backup. For long-term reliability, always keep the files in `images/`.
- Tip: rename files to simple names like `logo-01.png` for cleaner URLs, then update the `file` values.

## Colours and fonts

- Palette: Jet Black `#000000`, Soft White `#F8F8F6`, Flame Orange `#FF4500`. Change them in the `:root` block at the top of the CSS.
- Fonts (Google Fonts): Bricolage Grotesque for headings, DM Sans for body text, Instrument Serif italic for the accent words.
