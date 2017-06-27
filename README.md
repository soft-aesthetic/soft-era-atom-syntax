# \~ soft era \~

### syntax theme for [Atom](https://atom.io/)

🌸 Light pastel syntax theme for soft, warm, cozy, or cute coding. 🌱

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

---

## Contributing

Happy to hear any input <3

💖 [@animalphase](https://twitter.com/animalphase) on twitter
