# spiritrag.github.io

The developer website, served by GitHub Pages at <https://spiritrag.github.io/> from `main` (every push goes live in
a minute or two). Plain HTML and one stylesheet; no build step (`.nojekyll` turns off GitHub's Jekyll pass).

## What's here

| Path                          | What it's for                                                                          |
| ----------------------------- | -------------------------------------------------------------------------------------- |
| `index.html`                  | The home page: the games, each with its privacy policy and support links.              |
| `app-ads.txt`                 | AdMob's ownership file. One line for the whole AdMob account, so it covers every game. |
| `espresso-shots/privacy.html` | Espresso Shots' privacy policy: the App Store's Privacy Policy URL, AdMob's GDPR form. |
| `espresso-shots/support.html` | Espresso Shots' support page: the App Store's Support URL.                             |
| `style.css`, `404.html`       | The shared look, and the page for a wrong address.                                     |

## Rules

- **Never move or rename a page that a store listing points to.** The App Store listing, AdMob and the game itself
  link to these URLs. Add new pages instead.
- **`app-ads.txt` stays at the root**, and the App Store listing's website must be this site, or AdMob can't find it.
  Don't add a `robots.txt` that blocks it.
- **Quiet until launch:** every page carries `<meta name="robots" content="noindex">`, which asks search engines not
  to list it. At launch, remove it and give the game a proper page (screenshots, the App Store link).
- **When the game changes what it collects** (a new service, new data), update its privacy policy and the date at its
  top, and the App Privacy answers in App Store Connect.

## A new game

Add a folder named after it (`new-game/privacy.html`, `new-game/support.html`, copied from `espresso-shots/` and
rewritten for that game), and list it on `index.html`. `app-ads.txt` needs nothing new if its ads use the same AdMob
account.
