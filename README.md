# About

These are my `userChrome.css` customizations for Firefox.

# Installation

To link this `chrome` folder to your Firefox profile name, run the following command:

```
stow . -t "$HOME/.mozilla/firefox/$(awk -F= '/^\[Install/ {f=1} f && /^Default=/ {print $2; exit}' ~/.mozilla/firefox/profiles.ini)"
```
