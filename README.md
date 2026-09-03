# a11y-checklist

A single HTML file: twenty-four accessibility checks worth running before a front-end change
ships, grouped into structure, keyboard, forms, media, colour, and motion.

I built it because the useful version of this list has to be openable by someone who is not
going to clone a repo or install Node — a designer, a PM, a contractor on their last day. So
it is one file, with no build step, no dependencies, and no network requests.

It is not a replacement for WCAG. It is the set of failures that kept coming back in review.

## Usage

Download `index.html` and open it. That is the whole setup.

```sh
curl -O https://raw.githubusercontent.com/irisdomain23/a11y-checklist/main/index.html
open index.html
```

Or host it on any static server and bookmark it:

```sh
python3 -m http.server
```

Ticked items are saved to `localStorage` in that browser, so you can close the tab mid-review.
Nothing leaves the machine — there is no analytics, no fonts, and no fetch call in the file.

`Hide done` collapses the list as you work. `Reset` clears it. Printing gives you a clean
paper copy with the controls stripped out.

## Notes

- The checklist works with JavaScript disabled. The checkboxes are in the HTML; JavaScript
  only adds the progress count, the filter, and persistence.
- Done state is shown three ways — the checkbox, a strikethrough, and the word "done" — so it
  never depends on colour.
- It tries to pass its own checks: skip link, landmarks, labelled controls, visible focus,
  a polite live region for progress, and a layout that survives 320px and 200% zoom.

If a check here is wrong or missing one, open an issue. I would rather fix the list than keep
a tidy one.

## Licence

MIT.
