# Homebrew Tap for Swamp

Official [Homebrew](https://brew.sh) tap for [swamp](https://github.com/swamp-club/swamp), the AI Native Automation CLI.

## Install

```bash
brew tap swamp-club/tap
brew trust swamp-club/tap
brew install swamp
```

Homebrew 6 and later require third-party taps to be trusted before Homebrew will
load any formula from them. If you skip `brew trust`, the install fails with:

```
Error: Refusing to load formula swamp-club/tap/swamp from untrusted tap swamp-club/tap.
```

Homebrew 5 and earlier have no `brew trust` command; on those versions, skip that
step and the two remaining commands work as-is.

## Upgrade

```bash
brew upgrade swamp
```

Trusting the tap also matters here. When `brew upgrade` is run with no arguments,
it enumerates every installed formula and skips untrusted taps with a warning
rather than failing, so an untrusted swamp is quietly left behind at its old
version. Running `brew trust swamp-club/tap` once is what keeps upgrades flowing.

## How it works

This tap is updated automatically on every [swamp release](https://github.com/swamp-club/swamp/releases). Binaries are downloaded from `artifacts.swamp-club.com`.

## Supported platforms

| Platform | Architecture |
|----------|-------------|
| macOS | Apple Silicon (aarch64) |
| macOS | Intel (x86_64) |
| Linux | aarch64 |
| Linux | x86_64 |

## Alternative installation methods

- **Install script:** `curl -fsSL https://swamp-club.com/install.sh | sh`
- **Direct download:** [GitHub Releases](https://github.com/swamp-club/swamp/releases)
- **Built-in updater:** `swamp update`

## Links

- [swamp on GitHub](https://github.com/swamp-club/swamp)
- [swamp-club.com](https://swamp-club.com)
- [Discord](https://discord.gg/swamp-club)
