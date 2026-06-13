# The desk

Public, Slack-shareable wrappers for **The desk**, the Cirrus monthly newsletter
(subtitle: *The Cirrus Monthly*). Each issue has its own dated permalink and carries
its own Open Graph / Twitter Card metadata and preview image, so a shared link
unfurls with that issue's title, standfirst and teaser card. The reports themselves
stay behind Google sign-in.

## Structure

    /                  redirects to the latest issue (and mirrors its preview card)
    /2026-06/          June 2026, Issue 01, "Before it becomes a ticket"
      index.html       OG / Twitter meta + iframe embed of the live report
      og.png           1200x630 preview card for this issue

URL convention: one folder per issue, named by year-month (YYYY-MM).

## Adding an issue

1. Create /YYYY-MM/ with its own index.html (set og:url, og:image, og:title and
   og:description) and a 1200x630 og.png preview card.
2. Repoint the root redirect and the root OG block at the new issue.

Latest: https://cirrus-assessment.github.io/the-desk/2026-06/
