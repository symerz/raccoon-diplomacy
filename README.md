# raccoon-diplomacy

The public page. **This is the whole of our web presence** and it is not much,
because we're about twelve people who have met a few times.

It deploys to `symerz.github.io/raccoon-diplomacy`.

---

## What's in here

```
index.html      the page
print-pack.pdf  two cards on one A4 sheet, free to print
discord-qr.png  QR to the Discord invite
README.md       this file
```

That's it. No build step, no framework, no JavaScript, no fonts fetched from a
CDN, no analytics, no cookies. The page works offline once loaded.

**That's deliberate.** A harm reduction group run by volunteers shouldn't need a
toolchain to say hello, and shouldn't hand a visitor's IP to a third party to
render a paragraph of text.

## Why this is a separate repo

The working repo is private. It holds drafts, unreviewed clinical claims, session
logs, and founder disclosures that haven't been decided yet
(`FOUNDATION.public-draft.md` has the open questions).

This repo holds nothing that hasn't been read and agreed. If it ever grows
something uncertain, that belongs in the private repo until it's settled.

## Deploying

Push to `main` and it's live. GitHub Pages is configured once, at:

**Settings → Pages → Build and deployment → Source: Deploy from a branch →
`main` / `/ (root)`**

No Actions workflow. No YAML. If GitHub ever nags you to switch to a CI-based
deploy, the no-build setting still works.

## Before the first deploy

Two placeholders, both in `index.html`:

1. **`INVITE_URL_HERE`** — replace with the real Discord invite link. It appears
   once, in the `.cta` button.
2. **`discord-qr.png`** — generate it locally. Any offline QR generator, or
   `qrencode`:

   ```bash
   qrencode -o discord-qr.png -s 8 -m 2 'https://discord.gg/YOUR-INVITE'
   ```

   Generate it **locally, not from a web QR service** — a third-party QR generator
   sends your invite URL to somebody else's server, and it's the kind of thing
   nobody thinks about in a project like this.

Then drop `print-pack.pdf` in. To make it, print `print-pack.html` to PDF from a
browser — A4, 100%, background graphics off. There's no PDF toolchain in this
project on purpose; a browser already knows how to do it.

## Editing

The page's copy comes from `content/one-pager/what-this-is.md` in the private
working repo. **That file is the source; `index.html` is a copy of it.** If you
change one, change the other, or the drift becomes a lie in one direction or the
other.

Two lines in particular have been load-bearing:

- *"We don't have a website"* → *"this page is most of our public presence."* The
  second is better, and it's still true.
- *"We speak at places we've been invited to."* This replaced naming Camp Gaea
  directly. Same meaning, wider cover, no host venue attributed.

## What is deliberately absent

No departments. No org chart. No funding roadmap. No testimonials. No comic book.
No list of future Embassies. No host venue named anywhere.

**A host venue is not mentioned on this page, deliberately.** Same rule as
Camp Gaea in the printed material: we speak there, we don't represent it, we
don't answer for it, and a public page is the last place that distinction should
be ambiguous.

No phone numbers either. We haven't set a service area, and a number on a page
that outlives us is worse than no number. The card sheet says the same thing.

## If you find a mistake

Tell us in the Discord and we'll fix it. None of this has been reviewed by a
clinician, and the people most likely to spot something wrong are the people who
use it.

## License

The text and artwork are ours to share — copy it, print it, translate it, run a
workshop from it, start your own Embassy.

**Don't publish it as your own.** Keep the raccoons and say where you got it.