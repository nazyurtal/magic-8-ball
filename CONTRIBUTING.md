# Contributing

Thanks for your interest in improving Magic 8 Ball. It's a small, single-file
project, so contributing is simple.

## Project structure

Everything lives in `index.html` — HTML, CSS, and JavaScript in one file. There
is no build step and no dependencies.

- **Markup** — the ball, the question input, the language dropdown, and the
  history list.
- **Styles** — CSS variables drive the light/dark themes; the ball and the blue
  triangle are pure CSS.
- **Script** — the `i18n` object holds every language's UI strings and answers;
  `setReadout()` auto-fits the answer text to the triangle.

## Making a change

1. Fork the repo and create a branch: `git checkout -b my-change`.
2. Edit `index.html`.
3. Open the file in a browser and test:
   - Ask questions in each language and confirm the answer fits the triangle.
   - Toggle light/dark.
   - Check Arabic renders right-to-left.
   - Resize down to a phone width; confirm the layout still works.
4. Commit with a clear message and open a pull request.

## Adding a language

Add a new entry to the `i18n` object with `htmlLang`, `dir` (`"ltr"` or
`"rtl"`), `code`, `title`, `intro`, `qlabel`, `placeholder`, `prompt`,
`historyTitle`, `clearAll`, `empty`, `del`, and a 20-item `answers` array. Then
add a matching `<button class="lang-option" data-lang="…">` to the dropdown.

## Style

Keep it dependency-free and single-file. Match the existing restrained visual
style — one blue accent, quiet greys, no unnecessary motion.
