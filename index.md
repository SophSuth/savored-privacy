# Privacy Policy for Savored

**Last updated:** 2026-11-03

Savored is an iOS app for saving and organizing recipes. This policy explains what data the app handles, where it goes, and your rights.

## What we collect

Savored only handles data **you** add to it: links you paste or share into the app (Instagram, TikTok, YouTube or a recipe website), photos you pick, recipe text you type, and the recipes you save or edit.

We do **not** collect:

- Accounts or sign-in info — Savored has no login.
- Your name, email address, contacts or location.
- Analytics, telemetry, or crash reports.
- Advertising identifiers or tracking data of any kind.

Savored never uses your microphone. If you dictate text, that's Apple's keyboard feature; the app only receives the typed result.

## How a recipe is made

When you add a recipe, the app sends what you gave it to **our server** (a small service we run on Railway). The server turns it into a clean recipe — title, ingredients, steps and tags — using **Anthropic's Claude**, and sends the recipe back to your phone, where it's saved. If you write a recipe yourself with "Write it myself," nothing is sent anywhere.

Depending on what you added, the server may:

- **For a photo:** send the photo to Claude.
- **For typed text:** send the text to Claude.
- **For a recipe website:** fetch the page and send its recipe text to Claude.
- **For an Instagram, TikTok or YouTube video:** read the post's caption (or the video's description) first. If that doesn't contain the whole recipe, the server downloads the video, transcribes its audio, reads any text shown on screen, and takes a few still frames, then sends those to Claude. The video, audio and frames are **deleted as soon as the recipe is made** and are never kept. Videos longer than 3 minutes are not read: if one had to be downloaded to find its length, it is deleted straight away. The recipe then comes from the caption or description (and any recipe page it links to) only.
- **For a link in a post's caption** that points to a recipe page: fetch that one page (never pages linked from it) and send its recipe text to Claude.

**These requests are made by our server, not by your phone.** Instagram, TikTok, YouTube, recipe websites and the services listed below see a request from our server — not your IP address, and nothing identifying you or your device.

**One exception — the cover picture.** To give a saved recipe a cover picture, the app downloads the post's or page's image **directly from your phone**. That site sees an ordinary image request from your device, as it would in a web browser.

## What our server keeps

The server keeps no recipes, photos, captions, transcripts or text you send. It keeps only what it needs to work and to stop misuse:

| What | Why | How long |
|---|---|---|
| An anonymous identifier for your installation of the app, issued through Apple's App Attest (no name, account or contact details) | To confirm requests come from the genuine Savored app | While you use the app; deleted after 12 months without use |
| How many recipes each installation saved each day, and how many recipe requests it made (including ones that failed) | To apply the daily limits: 20 saves and 60 recipe requests per device, with an overall cap across all users, so the service can't be misused | 30 days |
| A daily total, per platform, of videos read and videos over the 3-minute limit. It holds no link, identifier or device | To judge whether the limit is right | 12 months |
| Technical server logs (for example, which post was processed and how long it took) | To keep the service running and fix problems | Kept by Railway for a limited period under its own policy |

Reinstalling the app creates a new anonymous identifier.

## Where your data lives

| Data | Where it's stored |
|---|---|
| Your saved recipes (title, ingredients, steps, tags, photos, notes) | Only on your device, in the app's local storage. Nothing leaves your device once saved. |
| What you send to make a recipe (links, photos, text, and video content read from posts) | Passed through our server to the services below while the recipe is being made, then discarded. |
| The anonymous identifier and daily counts | On our server, as described above. |

## Third parties

- **Anthropic** makes Claude, which turns your input into a recipe. It receives the content described above from our server. Anthropic's terms say API data is not used to train its models by default. See <https://www.anthropic.com/legal/privacy>.
- **Railway** hosts our server and stores the small amount of data described above. See <https://railway.com/legal/privacy>.
- **Apple** provides App Attest, which lets our server confirm requests come from the genuine Savored app. Your phone talks to Apple for this as part of iOS. See <https://www.apple.com/legal/privacy/>.
- **Decodo** provides the network connection our server uses to look up an Instagram post or YouTube video and to download YouTube video, so it can be read properly. Decodo sees the address of the post or video being looked up, sent from our server. See Decodo's privacy policy at <https://decodo.com>.
- **Apify** is a service our server falls back to when it can't read an Instagram post itself. Apify receives the post's address from our server. See <https://apify.com/privacy-policy>.
- **Google** runs the YouTube Data API, which our server uses to read a YouTube video's description. Google receives the video's ID from our server. See <https://policies.google.com/privacy>.
- **Instagram, TikTok, YouTube and recipe websites** receive a request for the post or page you chose to save, made by our server.

## Retention

- **On your device:** kept as long as Savored is installed. Delete individual recipes in the app, or uninstall the app to remove your whole library.
- **On our server:** as listed under "What our server keeps".
- **Third-party services:** under those providers' own policies.

## Your rights

- Delete any recipe in the app — it's gone immediately.
- Uninstall Savored — your whole local library goes with it.
- We hold no account, name or recipes for you on our server. The anonymous identifier and daily counts can't be linked to you, so we can't look up one person's data — but uninstalling the app means its identifier is never used again, and it's deleted after 12 months.

## Children

Savored is not directed to children under 13. We do not knowingly collect data from children.

## Contact

Questions about this policy? Email **sophiesutherland311@me.com**.

## Changes

If we update this policy, we'll change the date at the top and revise the relevant sections.
