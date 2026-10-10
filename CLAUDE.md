# vuolt.github.io

The studio's website, served by GitHub Pages from `main`. Static HTML, no
build step: what is committed is what is live, a minute or two after a push.
Published as **Vuolt**; the owner's name appears nowhere on the site (the
footer's App Store link is the id-only developer URL for that reason).

## Pages

- `index.html`: the front page. Since 10 Oct 2026 it opens on **Meal
  Metrics** (its launch): the app's gradient, "Snap it. Say it. Scan it.",
  the phone-and-card still, the App Store button, and the PUMPKIN launch
  code with its redeem link (`apps.apple.com/redeem?ctx=offercodes&id=6811470547&code=PUMPKIN`;
  the code ends 1 Nov 2026, take the panel out then). Below: the three ways
  to log, every app as a card (the platform filter reads `data-platforms`),
  About and the coffee button. Each card's `id` is linked from the store
  listings and from `privacy.html` / `support.html`, so keep the ids.
- `support.html`, `privacy.html`, `terms.html`, `impressum.html`: one
  section per app, each `h2` with an id (the store listings link straight to
  `privacy.html#mealmetrics` and so on). They share `site.css`.
- `pdf-offline-studio/help.html`: PDF Offline Studio's manual, with its own
  styles.
- `icons/`: app icons that aren't on the App Store yet or are kept local.
  `images/mealmetrics-hero.jpg`: the 16:9 store asset, used as the link
  preview (`og:image`). `images/mealmetrics-phone.webp`: the transparent
  phone still in the hero, rendered from the snap ad in the track-my-food
  repo (`Marketing/ads/snap.html` at 5.3 s, headline hidden, 2×).

## Look

Meal Metrics' own: tokens in `index.html` and `site.css` (`--paper`,
`--ink`, `--muted`, `--surface`, `--line`, `--berry`, and `--hero`, the
orange → raspberry → violet gradient). Outfit for headings, Instrument Sans
for text, both from Google Fonts. The hero is the one loud thing; everything
else stays quiet. The old navy-and-amber look (Anton + Inter) is gone.

## Working here

- Commits as `th3jlux` with the GitHub noreply address, passed as
  `GIT_AUTHOR_*` / `GIT_COMMITTER_*` environment variables; never change the
  git config, never a personal email in a commit. Claude never pushes; the
  owner pushes.
- Each app has its own Claude session and repo; this repo is edited only
  when the owner says so, for that app's section or card.
- Branches: `main` only. `pdf-studio-branch-update` (30 Sep) still holds
  unmerged work from the PDF Offline Studio and Avogadro sessions: the help
  page in de/es/fr/it/pt with a language switcher, and Avogadro's sections
  in privacy and support. Merge it from one of those sessions when wanted
  (it touches content, not the style blocks, so it should merge cleanly
  onto the new look); then delete it. The remote copies of the finished
  branches `ja-bitte-card` and `mealmetrics-policy` can be deleted on GitHub.
- Pending for Meal Metrics: the sharing paragraph in the privacy section
  once sharing ships (draft in track-my-food's `TODO.md`), and new address
  lines in the imprint and privacy page after the move.
