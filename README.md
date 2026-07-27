# The desk

Public, Slack-shareable wrappers for **The desk**, Cirrus's monthly newsletter.
Each issue has its own dated permalink and carries
its own Open Graph / Twitter Card metadata and preview image, so a shared link
unfurls with that issue's title, standfirst and teaser card. The reports themselves
stay behind Google sign-in.

## Structure

    /                  redirects to the latest issue (and mirrors its preview card)
    favicon.ico        shared site icons (also favicon-16/32.png, apple-touch-icon.png)
    /2026-06/          June 2026, Issue 01, "Before it becomes a ticket"
      index.html       OG / Twitter meta + favicon links + a top-level redirect to the live report
      og.png           1200x630 preview card for this issue
    /2026-07/          July 2026, Issue 02, "Beyond the role: Jad Kaddour"
      index.html       OG / Twitter meta + favicon links + a top-level redirect to the live report
      og.png           1200x630 preview card for this issue

The issue page redirects (it does not iframe) the reader to the Google
sign-in report. A top-level navigation lets the normal Cirrus sign-in run
first-party; embedding the report in an iframe breaks it, because the Google
login cannot render inside a cross-origin frame and third-party cookies are
blocked by default. The redirect is JavaScript-only so link-preview crawlers
still read the OG tags rather than following the reader to the login page.

URL convention: one folder per issue, named by year-month (YYYY-MM).
The icon is the orange "d" from the wordmark on the cream ground.

## Adding an issue

1. Create /YYYY-MM/ with its own index.html (set og:url, og:image, og:title and
   og:description) and a 1200x630 og.png preview card.
2. Repoint the root redirect and the root OG block at the new issue.

Latest: https://cirrus-assessment.github.io/the-desk/2026-07/
