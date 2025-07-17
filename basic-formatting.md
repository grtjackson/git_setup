# Basic Writing & Formatting Syntax

A quick reference for GitHub-flavored Markdown (GFM):

---

## Quoting text

To quote text, start a line with `>`:

```markdown
> This is a quote.
```

---

## Quoting code

Inline code with single backticks:

```markdown
Use `git status` to list modified files.
```

Block code with triple backticks:

````
```bash
git status
git add .
git commit -m "Message"
```
````

---

## Syntax highlighting

Add a language after the opening backticks:

```js
echo "Hello, world!";
```

---

## Supported color models

Wrap color codes in backticks and GitHub will render a swatch:

- `` `#0969DA` `` — blue circle
- `` `rgb(9, 105, 218)` ``
- `` `hsl(212, 92%, 45%)` ``

---

## Links

Inline-style:
```markdown
[GitHub Pages](https://pages.github.com/)
```

Bare URLs auto-link:
```
https://github.com
```

---

## Section links (anchors)

Headings auto-generate linkable anchors. For example:

```markdown
## My Section Title
```

Becomes `#my-section-title`.

---

## Relative links

Link to files within your repo:
```markdown
[Contributing Guide](docs/CONTRIBUTING.md)
```

---

## Line breaks

In `.md` files, force a line break by ending a line with two spaces:

```markdown
First line␣␣
Second line
```

---

## Lists

**Unordered:**
```markdown
- Bullet One
- Bullet Two
```

**Ordered:**
```markdown
1. First item
2. Second item
```

Use indentation for nesting.

---

## Emphasis

- *Italic* or _italic_
- **Bold** or __bold__
- ***Bold + italic***
- ~~Strikethrough~~

---

*This file is adapted from GitHub’s own documentation at GitHub.com.*
