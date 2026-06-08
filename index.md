# Privacy Policy for Savored

**Last updated:** 2026-06-08

Savored is a personal iOS app for saving and organizing recipes. This policy explains what data the app handles, where it goes, and your rights.

## What we collect

Savored only handles data **you** add to it: URLs you paste, photos you pick, Instagram posts you share into the app, and recipes you save or edit.

We do **not** collect:

- Accounts or sign-in info — Savored has no login.
- Analytics, telemetry, or crash reports.
- Advertising identifiers.
- Tracking data of any kind.
- Your contacts, location, or device information.

## How we use it

When you add a recipe by pasting a URL, picking a photo, or sharing a post from another app, Savored sends the relevant content — the URL, any photo you picked, an Instagram caption, or extracted video frames and audio transcript — to **Anthropic's Claude API**, which extracts a clean recipe (title, ingredients, steps, etc.) from it.

For Instagram URLs, Savored also sends the URL to **a small backend service we host on Railway** (`cookbook-ig-fetcher`) to fetch the video and caption — Instagram doesn't expose those directly to the iOS share sheet.

For web recipe URLs, Savored sends the URL to the same Railway service to discover the page's hero image so we can attach it to the saved recipe.

That's it. The extracted recipe is then saved locally on your device.

## Where your data lives

| Data | Where it's stored |
|---|---|
| Your saved recipes (title, ingredients, steps, tags, photos, notes) | Locally on your device, in iOS's SwiftData store. Nothing leaves your device once saved. |
| URLs, photos, captions, video content sent for extraction | Transmitted in real time to Anthropic and to Savored's Railway backend. Neither service stores your recipes; the backend is a stateless proxy. Both providers have their own privacy policies governing how they handle API requests in transit. |
| Per-device extraction counter (to enforce a daily rate limit) | UserDefaults on your device only. Never transmitted. |

## Third parties

- **Anthropic** is the company behind Claude, the model that extracts recipes from your inputs. API requests are subject to Anthropic's data handling policy, which states that API customer data is not used to train their models by default. See <https://www.anthropic.com/legal/privacy>.
- **Railway** hosts the small backend service Savored uses for Instagram fetching and web image lookup. The backend is stateless — it doesn't persist your data. See <https://railway.com/legal/privacy>.

## Retention

- **On-device data:** kept as long as you have Savored installed. Delete individual recipes inside the app; uninstall the app to remove your entire local library.
- **Third-party services:** subject to Anthropic's and Railway's own retention policies.

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
