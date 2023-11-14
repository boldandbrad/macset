# macset

A utility to set macOS user defaults declaratively from a YAML file, written in python.

> Inspired by [apply-user-defaults](https://github.com/zero-sh/apply-user-defaults)

## Install

- Homebrew via custom tap (coming soon)
- Pipx (coming soon)
- Pip (coming soon)

## Usage

Given a user defaults YAML file structured like the following:

```yaml
com.apple.dock:
  mineffect: "scale" # minimize windows using scale effect
  show-recents: false # don't show recents in dock

com.apple.AppleMultitouchTrackpad:
  Clicking: true  # enable tap to click
```

Apply the defaults with:

```zsh
macset --file path-to.yaml
```

## Roadmap

- Template expansion
- `--verbose` shows the commands that are being run
- `--dry-run` flag that checks the current value of each default and shows what changes would be made, without making them.
- Obeys `$MACSET_FILE` env variable to store default yaml file location

## License

Copyright (c) 2022 Bradley Wojcik. Released under the MIT License. See
[LICENSE](LICENSE) for details.
