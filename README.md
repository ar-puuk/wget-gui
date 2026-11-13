# Fetch: a Wget command builder

Build Wget commands visually instead of memorising flags. Fetch covers every option in `wget --help` for version 1.21 (155 settings), explains what each one does, warns about risky choices, and exports a queue of jobs as one `.bat` or `.ps1` script. It runs entirely in your browser. Nothing is uploaded.

Fetch is part of **Conduit**, a pair of command builders that share one design system. Its sister app is [Mirror, the Robocopy builder](https://github.com/ar-puuk/robocopy-gui).

## How to use it

1. **Pick a starting point.** Choose a preset such as Offline site copy or Images only, or start from scratch.
2. **Fill in the tabs.** Target, What to download, Save layout, Filters, Performance, Requests, Security, Logging and Advanced. Rarely used options stay hidden until you turn on Show advanced.
3. **Watch the command.** It updates as you choose, with every flag explained and notes for risky choices such as skipping certificate checks, passwords in the command, or crawling with no wait.
4. **Add to queue.** Build several downloads, reorder them, then download one script. Stop on first failure is on by default.

Other ways in:

* **Find an option.** Type a name or a flag, such as `cookies` or `--limit-rate`, to search every tab at once.
* **Paste a command.** Paste an existing `wget` command and the form fills in. Flags the builder does not recognise are kept under Advanced.
* **Command palette.** `Ctrl+K` jumps to any option, preset or page. `Ctrl+Enter` adds the current command to the queue.
* **Profiles.** Save a full set of options and load it later. Profiles, the queue and the form are remembered in this browser.

## Development

The whole app is one self-contained `index.html` with no build step to run it. It is generated from the shared source in the [robocopy-gui](https://github.com/ar-puuk/robocopy-gui) repo (`design/`), so that Fetch and Mirror keep identical design tokens and components. Make design changes there and run `node build.js`, rather than editing this `index.html` by hand.

## Credits

Icons are from [Lucide](https://lucide.dev) (ISC license), inlined unmodified. Fonts are Bricolage Grotesque, Instrument Sans and JetBrains Mono from Google Fonts.

## License

See [LICENSE](LICENSE).
