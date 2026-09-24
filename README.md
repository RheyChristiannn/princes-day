# For love, always — Princes at 20

A pink, responsive birthday website for Future Engr. Princes Aizy L. Boquilon. Pure HTML, CSS and Vanilla JavaScript, with Tailwind CSS via CDN. No build step, backend, account, API, or database needed. Custom CSS keeps the layout usable even if the Tailwind CDN is unavailable.

## Project structure

```text
princes-20/
├── index.html           # Complete page, styles, interactions and editable letter
├── images/
│   ├── .gitkeep
│   ├── princes.jpg      # Add your portrait here
│   ├── memory-01.jpg    # Add your memory photos here
│   ├── memory-02.jpg
│   └── memory-03.jpg
└── README.md
```

The four photos are yours to add; they are not included. Built-in illustrations appear until matching photos are available. Use exactly these lowercase filenames, or change the paths in index.html. Relative images/ paths work with GitHub Pages project URLs too.

## Personalize, love

### Birthday music

Ibutang ang actual MP3 file sa **`audio/birthday.mp3`**. The folder includes a reminder file. The MP3 itself is not included. If you choose another filename, update the `<audio>` element's `src` in `index.html`.

Opening the envelope or **Open your letter** starts the music. A Play/Pause button appears inside the letter. Closing it pauses playback; reopening resumes. If the file is missing or the browser blocks playback, the letter still works and displays a short message. Refresh after adding the MP3, and include the `audio` folder when publishing.

1. Open `index.html` in your browser to preview. No installation needed.
2. Search for `DIRI ISULAT ANG IMO PERSONAL LETTER` in the code. Replace or add `<p>...</p>` paragraphs underneath it.
3. Replace `Your love` in the letter signature with your name if desired.
4. Search for `PERSONALIZE HERE` to edit the three memory titles, captions, full messages and photo paths.
5. Add your own photos to `images/`. Portrait-oriented photos work best for `princes.jpg`; landscape or square photos work well for memories. Aim for under 1 MB per image for faster mobile loading.
6. Edit the `quotes` array for more personal encouragement.

## Included interactions

### Add any number of photos to an album

Place your images in `images/`, then search for `ALBUM PHOTOS` in `index.html`. Each of the three albums has its own `photos` list. Add as many entries as you need:

```js
photos: [
  "images/memory-01.jpg",
  "images/beach-day.jpg",
  "images/coffee-date.png",
  "images/together.webp",
],
```

The first listed photo is the cover. File names, capitalization and extensions must match the actual files. Refresh the page after saving. You can also copy a complete album object inside `memories` to add more albums.

There is no fixed photo limit in the code. Only the selected photo loads inside the viewer. Use Previous/Next, keyboard left/right arrows, or a horizontal swipe on the photo. Navigation loops from the last photo to the first. A one-photo album disables navigation; empty albums and missing files show an illustration. Photos are displayed uncropped in the viewer.

Dropping files into the folder alone does not register them: a static website cannot list local folder contents. Include each photo path in its album's `photos` list. These lists are saved with the website, so they also work after publishing; there is no temporary browser-only upload storage.

- Countdown to October 7, 2026, midnight Philippine time, with birthday-day celebration and a lasting greeting afterward.
- Six rotating encouragement messages for study breaks.
- Three photo memory cards with keyboard-accessible dialogs.
- Interactive bridge blueprint with foundation, journey and future messages.
- Birthday envelope opening an editable letter with falling hearts. Reduced-motion preferences are respected.

## Publish for free with GitHub Pages

1. Create a GitHub repository and upload `index.html` and the `images` folder. Keep the HTML file at the repository root.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select **main** and **/(root)**, then save.
5. Wait for deployment and open the website link shown on the Pages settings screen. Test the link on your phone before sharing it with her.

## Or use Vercel

1. Put these files in a GitHub repository.
2. Sign in to Vercel and create a new project by importing the repository.
3. Choose **Other** for framework preset; no build command is needed. Use the project root as the output location (`.` if a value is required).
4. Deploy and use the generated website link.

Hosting the site makes its photos and letter accessible to visitors with the URL. Publish only the content you want to share. This project has not been published automatically.

## Preview checklist

- Check phone widths around 375–430 px and desktop widths around 1280–1440 px.
- Open every memory and the letter; close using ×, Escape, or the backdrop.
- Try all blueprint buttons and the reminder button.
- Confirm your photos and personal letter before publishing.
