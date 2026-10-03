# Brutalfox

Remove rounded corners and shadows from Firefox and pages, and add a few small animations. written with Firefox 157 with the Nova design in mind

## Installation

### Regular Firefox

1. Open `about:profiles` in Firefox
2. Find the profile marked as in use and click Open Folder next to its Root Directory
3. In that folder, create a folder named `chrome` if it does not exist
4. Copy `userChrome.css`, `userContent.css` and `animations.css` to the `chrome` folder

If Open Folder does nothing, open the profiles folder yourself. The usual locations are:

- Linux: `~/.mozilla/firefox/`
- macOS: `~/Library/Application Support/Firefox/Profiles/`
- Windows: `%APPDATA%\Mozilla\Firefox\Profiles\`

The Linux path does not apply to the Snap build that some distributions ship. Use Open Folder from `about:profiles` there, or look under `~/snap/firefox/common/.mozilla/firefox/`

### Flatpak

The Flatpak build keeps its profiles in a different place:

```
~/.var/app/org.mozilla.firefox/.mozilla/firefox/
```

### Result

Your `chrome` folder should now contain:

- `userChrome.css`
- `userContent.css`
- `animations.css`

## Enable custom CSS in Firefox

Go to `about:config` and set the following preference to `true`:

```
toolkit.legacyUserProfileCustomizations.stylesheets
```

Firefox ignores `userChrome.css` and `userContent.css` without it

Then close every Firefox window and open it again. Firefox only reads the files at startup

Thanks to [Acercandr0](https://github.com/Acercandr0) for [Latin Accent](https://github.com/Acercandr0/Latin-Accent), which inspired the animations in this project