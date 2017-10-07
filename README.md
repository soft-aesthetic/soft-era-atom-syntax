# \~ soft era \~

### syntax theme for [Atom](https://atom.io/)

🌸 Light pastel syntax theme for soft, warm, cozy, cute coding. 🌱

Begun by heavily modifying [new era light](https://github.com/juanmnl/new-era-light-syntax-theme).

![soft era syntax theme screenshot](screenshot.png)

## Installation

- Go to **Settings > Install > Themes tab**
- Search for `soft-era-syntax` and click Install
- Go to **Settings > Themes** and choose **Soft Era** from the dropdown menu

###### or, from the command line:

```apm install pure-syntax```


💾 enjoy <3

---

## User stylesheet modifications

### Fixes:

Some UI may cause the cursor to appear as invisible, or the same as the background color, in search boxes. If you have this issue, you can add this to your stylesheet:

```
.cursor {
  color: rgba(244,129,187,1);
  border-left: 2px solid rgba(244,129,187,1) !important;
}
```

### Suggested modifications for the default UI theme (One Light)

```
// style the active tab in One Light UI theme
@soft-purple-darker: #b4addf;
.tab-bar .tab.texteditor.active {
  background-color: #f9f5f5 !important;
}
.tab.texteditor.active::before {
  background: @soft-purple-darker !important;
  width: 4px !important;
}
.tab-bar .close-icon {
  color: @soft-purple-darkest !important;
}
.tab-bar .close-icon:hover {
  color: @soft-text-dark !important;
  background: #fff !important;
}
```

### Other modifications that compliment this theme nicely:

```
// BPMono is a cute rounded fond that looks nice in italics.

// Italic BPMono for comments:
atom-text-editor::shadow .comment {
  font-family: "BPMono";
  vertical-align: top;
  font-style: italic;
}

// Italic BPMono for function declaration:
// targets the word "function" when declaring a function
.syntax--type.syntax--function.syntax--js:not(.syntax--arrow) {
  font-family: "BPMono";
  font-style: italic;
}

// I like to use the Fira Code ligatures,
// even if i'm using another main font
.syntax--keyword.syntax--operator {
    font-family: "Fira Code";
}
```

![soft era syntax theme screenshot](screenshot2.png)

---

## Contributing

### TODO:
- [x] create variable for operator and whatever other `@soft-` is still in use in the `base.less` file
- [ ] this theme reports deprecations in the CSS selectors, pull in new version of atom one theme to compare/revise
  - [ ] if that doesn't work, just update selectors in this theme
- [ ] examine differences between the packages `react` (~500k downloads) and `language-babel` (~1.5m downloads), as they lead to different colors in a lot of cases.
- [ ] build in better support for  `language-babel`
  - [ ] theme selectors, particularly special javascript selectors, are built with the `react` way of handling things—this should not be treated as primary since it isn't default
  - [ ] see how styling works **without either of these packages activated**
- [ ] parameter vs arguments are fucked up
- [ ] determine other packages that require or would benefit from specific support.
  - [ ] group these into separate .less files. currently there are already special styles for the `indent-guide-improved` package, inside of `index.less`
- [ ] make html tag punctuation and text same color? (maybe depend on determining the differences of above-named packages)
- [ ] add support for package `language-markdown` -> [package contribution reference](https://github.com/burodepeper/language-markdown/blob/master/CONTRIBUTING.md#syntax-theme-support)
  - [ ] currently the quote characters put in `syntax--string` classes and that makes it not work well (especially when writing with punctuation)
- [ ] see about removing all direct color variables like `@cyan` from `base.less`
- [ ] move all color definitions into one place, written in a standardized way, to make it easier to keep track, make alternate versions of the theme, and port to other programs.
  - [ ] verify this is being done in the best way to match up with the latest theme code
- [ ] separate out "special treatments" and overrides. (most are currently at bottom of file, but there are some atom-specific treatments like before and after elements, special function coloring, italicizing words, changing font weight — appropriate to pull these out and group at bottom of file or in separate .less file?)
  - [ ] these seem to be a bit of a mess and first fixing some of the package support/conflicts above may help this organization
- [ ] nicer clickable link treatment (for markdown previews and wherever else they are clickable)

Much of this cleanup and organization is in the push to make this theme easier to 1) organize for porting to other editors, and 2) using the same organizational thought behind the syntax highlighting to quickly create other themes.

---

Currently styled with `.js`, `.css`, `.html`, `.json`, `.md`, `.svg` files in mind as that's my main use case. Would like to hear more about other files/languages.

Happy to hear any input <3

💖 [@animalphase](https://twitter.com/animalphase) on twitter
