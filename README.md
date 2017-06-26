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

### Suggested modifications for the default UI theme (One Light) to paste into your user stylesheet:

```
// style the active tab in One Light UI theme
@soft-purple-darker: #b4addf;
.tab-bar .tab.active[data-type$="Editor"], .tab-bar .tab.active[data-type$="AboutView"], .tab-bar .tab.active[data-type$="TimecopView"], .tab-bar .tab.active[data-type$="StyleguideView"], .tab-bar .tab.active[data-type="MarkdownPreviewView"] {
  background-color: #f9f5f5 !important;
}
.tab.texteditor.active::before {
  background: @soft-purple-darker !important;
  width: 4px !important;
}
.tab-bar .close-icon:hover {
  transform: scale(1.2) !important;
}
```

### Other modifications in my user stylesheet that compliment this theme nicely:

```
// BPMono is a cute rounded fond that looks nice in italics.

// Italic BPMono for comments:
atom-text-editor::shadow .comment {
  font-style: italic;
  font-family: "BPMono";

}

// Italic BPMono for function declaration:
// targets the word "function" when declaring a function
.syntax--type.syntax--function.syntax--js:not(.syntax--arrow) {
  // font-family: "Source Code Pro";
  font-family: "BPMono";
  font-style: italic;
}

// I like to use the Fira Code ligatures
// also like them a little heavy
.syntax--keyword.syntax--operator {
    font-family: "Fira Code";
    font-weight: 400;
}
```

---

## Contributing

NOTE: currently have only pasted in the overrides from my user stylesheet in atom, and it's only written out with javascript in mind.

Need to better author the .less, and put more thought into other languages. It's definitely usable in HTML & CSS at the moment.

Happy to hear any input <3

💖 [@animalphase](https://twitter.com/animalphase) on twitter
