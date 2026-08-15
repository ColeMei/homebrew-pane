# ColeMei/homebrew-pane

Homebrew tap for [Pane](https://github.com/ColeMei/pane) — a hotkey-summoned notes panel for macOS,
backed by a folder of markdown files you own.

```bash
brew install --cask ColeMei/pane/pane
```

Pane is unsigned, so macOS reports it as "damaged and can't be opened", and right-click → Open no
longer gets past that. It is not damaged — that is simply what an unsigned app looks like now. Clear
the quarantine flag once and it launches normally from then on:

```bash
xattr -dr com.apple.quarantine /Applications/Pane.app
```

Or skip the flag at install time:

```bash
brew install --cask --no-quarantine ColeMei/pane/pane
```

## Maintenance

`Casks/pane.rb` is a mirror. The source copy lives in the Pane repo at `packaging/pane.rb`, so the
caveat text is reviewed in the same change as the code it describes. After each release, copy it
here and update `version`, `url` and `sha256` — the release workflow prints the sha256 in its job
summary.
