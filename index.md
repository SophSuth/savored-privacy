# Privacy Policy for Savored

**Last updated:** 2026-08-12

Savored is a personal iOS app for saving and organizing recipes. This policy explains what data the app handles, where it goes, and your rights.

## What we collect

Savored only handles data **you** add to it: URLs you paste, posts you share into the app from Instagram, TikTok or YouTube, photos you pick, recipe text you write yourself, and recipes you save or edit.

We do **not** collect:

- Accounts or sign-in info — Savored has no login.
- Analytics, telemetry, or crash reports.
- Advertising identifiers.
- Tracking data of any kind.
- Your contacts, location, or device information.

## How we use it

When you add a recipe, Savored sends the relevant content to **Anthropic's Claude API**, which extracts a clean recipe (title, ingredients, steps, and so on) from it. Depending on how you added it, that content may include the URL, a photo you picked, a post's caption or description, and — for videos we can read — extracted frames and an audio transcript. This request goes **directly from your device** to Anthropic. If you write a recipe yourself using "Write it myself," none of it is sent anywhere — it's typed straight into your local library.

To read a post you've shared, Savored also uses **a small backend service we host on Railway** (`cookbook-ig-fetcher`). Social platforms don't expose captions or video to the iOS share sheet, so the app sends the post's URL to that service, which fetches what it can and sends it back. The same service looks up a page's main image for web recipe URLs, so your saved recipe has a cover.

**These requests are made by our server, not by your phone.** Instagram, TikTok, YouTube, Google and Apify (below) therefore see a request from our backend — not your IP address, and nothing identifying your device.

To do that work, the backend may contact:

- **YouTube's official Data API**, operated by Google, to read a video's description and thumbnail. Savored does not download YouTube videos.
- **Instagram and TikTok** directly, to read a post's caption, cover image, and — for Instagram — its video.
- **Apify**, a third-party service, as a fallback for Instagram posts our own fetching can't read.

That's it. The extracted recipe is then saved locally on your device.

## Where your data lives

| Data | Where it's stored |
|---|---|
| Your saved recipes (title, ingredients, steps, tags, photos, notes) | Locally on your device, in iOS's SwiftData store. Nothing leaves your device once saved. |
| URLs, photos, captions, video content sent for extraction | Transmitted in real time to Anthropic, and to Savored's Railway backend and the services it calls on your behalf. None of them stores your recipes; the backend is a stateless proxy that keeps nothing between requests. Each provider has its own privacy policy governing requests in transit. |
| Per-device extraction counter (to enforce a daily rate limit) | UserDefaults on your device only. Never transmitted. |

## Third parties

- **Anthropic** is the company behind Claude, the model that extracts recipes from your inputs. Requests go directly from your device. API requests are subject to Anthropic's data handling policy, which states that API customer data is not used to train their models by default. See <https://www.anthropic.com/legal/privacy>.
- **Railway** hosts the small backend service Savored uses to read shared posts and look up page images. The backend is stateless — it doesn't persist your data. See <https://railway.com/legal/privacy>.
- **Google** operates the YouTube Data API, which our backend uses to read a YouTube video's description and thumbnail. Google receives the video's ID from our server. See <https://policies.google.com/privacy>.
- **Apify** is a third-party service our backend falls back to when it can't read an Instagram post directly. Apify receives the post's URL from our server. See <https://apify.com/privacy-policy>.
- **Instagram, TikTok and YouTube** receive a request for the post you chose to save, made by our server.

## Retention

- **On-device data:** kept as long as you have Savored installed. Delete individual recipes inside the app; uninstall the app to remove your entire local library.
- **Third-party services:** subject to those providers' own retention policies.

## Your rights

- Delete any recipe in the app — it's gone immediately.
- Uninstall Savored — your entire local library is gone with it.
- There's no server-side account or stored recipe data for us to delete on request, because we don't keep any.

## Children

Savored is not directed to children under 13. We do not knowingly collect data from children.

## Contact

Questions about this policy? Email **sophiesutherland311@me.com**.

## Changes

If we update this policy, we'll change the date at the top and revise the relevant sections.
