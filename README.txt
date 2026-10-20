STEEL FANG - GOOGLE PLAY PACKAGE
Made by Anay Tripathi

Google Play does not accept HTML files directly. These files turn the game into an
installable web app. A free tool, PWABuilder, then converts it into the .aab file that
Google Play accepts.

WHAT'S IN THIS FOLDER
  index.html                  The game, set up as an installable app that works offline
  manifest.json               App name, icons and colours
  sw.js                       Offline support
  icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png   App icons
  privacy.html                Privacy policy (Google Play requires one)
  .nojekyll                   Lets GitHub Pages serve the ".well-known" folder (step 5)
  feature-graphic-1024x500.png        Play Store banner
  screenshot-1/2/3.png                Play Store screenshots

BEFORE YOU START
  Open privacy.html and replace [add your contact email here] with your email.

STEP 1 - Put the game online (free, GitHub Pages)
  1. Make a free account at github.com.
  2. Create a new PUBLIC repository named exactly:  YOURUSERNAME.github.io
     (Use your real GitHub username. This name matters for step 5.)
  3. In the repository: Add file > Upload files. Upload every file in this folder.
     If .nojekyll is hidden on your phone, create it instead:
     Add file > Create new file, name it  .nojekyll  , leave it empty, commit.
  4. Settings > Pages > Source: "Deploy from a branch", Branch: main, folder: / (root). Save.
  5. Wait 1-2 minutes, then open  https://YOURUSERNAME.github.io  . The game should load.

STEP 2 - Turn it into a Google Play file (free, PWABuilder)
  1. Go to pwabuilder.com and paste  https://YOURUSERNAME.github.io
  2. Click "Package for stores", then choose Android / Google Play.
  3. Package ID: something like  io.github.yourusername.steelfang
     App name: Steel Fang Tanks. Signing key: "Create new".
  4. Download the zip. It contains:
       - the .aab file you upload to Google Play
       - your signing key and its passwords. KEEP THESE SAFE FOREVER.
         You need them for every future update. If you lose them you cannot update the app.
       - assetlinks.json

STEP 3 - Remove the browser address bar inside the app
  1. In your GitHub repository: Add file > Create new file
  2. Name it  .well-known/assetlinks.json  (typing the slash creates the folder)
  3. Paste in the contents of assetlinks.json from the PWABuilder zip and commit.

STEP 4 - Publish on Google Play
  1. Create a Google Play developer account at play.google.com/console (one-time US$25).
  2. Create app > name "Steel Fang Tanks", type Game, Free.
  3. New personal accounts must run a closed test first: at least 12 testers opted in
     for 14 days in a row. Upload the .aab to Closed testing and invite friends and family.
  4. Store listing:
       App icon: icon-512.png
       Feature graphic: feature-graphic-1024x500.png
       Screenshots: screenshot-1.png, screenshot-2.png, screenshot-3.png
       Privacy policy URL: https://YOURUSERNAME.github.io/privacy.html
  5. Complete the content rating questionnaire and the Data safety form. Answer them
     using what privacy.html says (no accounts, no ads, no data collected).
  6. After the 14-day test, apply for production access and submit.

UPDATING THE GAME LATER
  Replace index.html on GitHub and change 'steel-fang-v7' in sw.js to a new name
  (for example 'steel-fang-v8'). Players get the new version automatically, with no
  new upload to Google Play needed.
