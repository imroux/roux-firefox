# About

These are my `userChrome.css` customizations for Firefox.

# Installation

To link this `chrome` folder to your Firefox profile directory, run one of the
following commands depending on the location of firefox profiles
(`~/.mozilla/firefox` or `~/.config/mozilla/firefox`):

```
stow . -t "$HOME/.mozilla/firefox/$(awk -F= '/^\[Install/ {f=1} f && /^Default=/ {print $2; exit}' ~/.mozilla/firefox/profiles.ini)"
```

OR

```
stow . -t "$HOME/.config/mozilla/firefox/$(awk -F= '/^\[Install/ {f=1} f && /^Default=/ {print $2; exit}' ~/.config/mozilla/firefox/profiles.ini)"
```

> In `about:config` set `toolkit.legacyUserProfileCustomizations.stylesheets` to
> `true`
