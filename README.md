# 🎂 Happy Birthday: A Surprise Gift Page

A one-page interactive birthday surprise, made to go with a real gift hunt: numbered boxes, a secret password and a behind-the-scenes video at the end.

Everything lives in **one HTML file**: no libraries, no build step, and no sound or image files. The sounds are made in the browser.

## ✨ Features

- **Animated welcome**: bouncing "Happy Birthday" title, floating balloons and a confetti burst when the page opens
- **Animated background**: drifting colour blobs, sparkle dots, and stars, hearts and squiggles floating up
- **Interactive cake**: tap to blow out the candles, with smoke, a whoosh, confetti and a "Happy Birthday" tune. Tap again to relight them.
- **Birthday message and rules card**: open the numbered boxes in order, no cheating!
- **Final reveal**: a two-step "I've opened all the boxes" confirmation, then a party horn and confetti
- **Password lock** for the secret folder:
  - a different funny message on every wrong try (Santa, Tinker Bell, the Easter Bunny…)
  - 4 fail sounds that take turns (sad trombone, buzzer, boing, slide whistle)
  - a hint after 3 wrong tries and a final hint after 5
  - the right password plays a victory fanfare, sets off confetti and shows the Google Drive link
- **Sound on/off** button
- Works on phones and computers, in light and dark mode, and respects the "reduce motion" setting

## 🎁 How the gift works

1. Your friend gets a short note (for example a `.md` file shared on Google Drive) that tells them to open the boxes in order, then come back.
2. They open the physical boxes in number order: 1, 2, 3…
3. **The last box holds the password.**
4. They come back to this page, confirm they've opened everything and enter the password.
5. The page unlocks and links to a Google Drive folder with the behind-the-scenes video.

> 💡 Google Drive can't password-protect a folder. For a real lock, put the video in a password-protected `.zip` (7-Zip with AES-256 on Windows, Keka on Mac) and use the same password on the page.

## 🛠️ Customize

Open `index.html` in any text editor and find the `EDIT THESE` block near the top of the `<script>`:

```js
const FRIEND_NAME = "";   // e.g. "Andreas" -> "Happy Birthday, Andreas!"
const DRIVE_LINK  = "https://drive.google.com/drive/folders/PASTE_YOUR_FOLDER_ID_HERE";
const SECRET      = "birthday";   // the password (capital letters don't matter)

const HINT_1 = "To help you a bit: what was the final present?";   // after 3 wrong tries
const HINT_2 = "Final hint: CHANGE ME - your last clue goes here";  // after 5 wrong tries

const WRONG_MESSAGES = [ ... ];   // add, remove or change as many as you like
```

The birthday message itself is in the HTML. Search for `To my friend` to change it.

## 🚀 Hosting

Google Drive shows `.html` files as code, not as a web page, so host the page somewhere else:

- **GitHub Pages** (free): push this repo, then go to **Settings → Pages → Deploy from branch → `main` / root**. The page will be live at `https://<your-username>.github.io/<repo-name>/`.
- **Netlify Drop**: drag the folder onto [app.netlify.com/drop](https://app.netlify.com/drop).
- **Locally**: just double-click `index.html`.

Then share the link in the note your friend reads first.

## 📁 Files

```
.
├── index.html   # the whole page: HTML, CSS, JavaScript and sounds
└── README.md
```

## ⚠️ Good to know

- **The password isn't truly secret.** Anyone who opens the page's code can find it. It's fine for a gift game, but the password-protected zip is the real lock.
- **Sound starts after the first tap.** Browsers don't allow sound before that, so the confetti when the page first opens plays without sound.
- **On iPhone**, sound should play even with the silent switch on, but turn the volume up!

## ❤️ Credits

Made with love (and a lot of confetti) for a friend's birthday.
# HappyBirthday
