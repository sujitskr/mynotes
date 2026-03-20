# 📝 Markdown Cheat Sheet

> A quick reference guide for Markdown syntax — covers both standard and extended Markdown.

---

## Table of Contents

- [Block Elements](#block-elements)
- [Basic Text Elements](#basic-text-elements)
- [Text Styling](#text-styling)
- [Code](#code)

---

## Block Elements

### Block Quote

```md
> This is a quote
>
>> Nested quote
```

> This is a quote
>> Nested quote

---

### Ordered List

```md
1. First
2. Second
   1. Numbers
   1. Don't matter
```

> Numbers don't have to be sequential — Markdown auto-increments them.

---

### Unordered List

```md
* Asterisks
* List
  * Nested

+ Can also use plus sign

- Can also use dash
```

> You can use `*`, `+`, or `-` as bullet markers.

---

### Images

```md
![Alt Text](https://example.com/image.png)
![Relative Image](/img.jpg)
```

**Output HTML:**
```html
<img src="https://example.com/image.png" alt="Alt Text" />
<img src="/img.jpg" alt="Relative Image" />
```

---

### Checklist *(Extended)*

```md
- [ ] Must include space
- [x] Completed
```

- [ ] Must include space
- [x] Completed

---

### Tables *(Extended)*

**Basic Table:**
```md
| Name  | Age |
| ----- | --- |
| Kyle  | 28  |
| Sally | 45  |
```

| Name  | Age |
| ----- | --- |
| Kyle  | 28  |
| Sally | 45  |

**With Alignment:**
```md
| Right | Center | Left |
| ----: | :----: | :--- |
| Kyle  |   28   | Hi   |
| Sally |   45   | Bye  |
```

| Right | Center | Left |
| ----: | :----: | :--- |
| Kyle  |   28   | Hi   |
| Sally |   45   | Bye  |

> `----:` = right-align, `:----:` = center, `:----` = left-align

---

## Basic Text Elements

### Headings

```md
# Heading 1
## Heading 2
### Heading 3 {#my-id}
#### Heading 4
##### Heading 5
###### Heading 6
```

> IDs (`{#my-id}`) are only supported in extended Markdown.

---

### Paragraphs

```md
This will be the same
paragraph if only one new line is used.

This starts a new paragraph
because two or more new lines were used.
```

---

### Line Breaks

```md
Two spaces at end of line  
will create a line break.
```

> Add **two trailing spaces** (`  `) at the end of a line to insert a `<br />`.

---

### Links

```md
[Label](https://example.com)
[Relative](/other-page)
[Jump to ID](#my-id)
<https://url.com>
https://extended.com
```

> Automatic linking (bare URLs) is only supported in extended Markdown.

---

### Horizontal Rule

```md
---

***

________
```

> Use at least 3 dashes, asterisks, or underscores. Must have blank lines above and below.

---

## Text Styling

| Style         | Markdown                        | Output                      |
| ------------- | ------------------------------- | --------------------------- |
| Bold          | `**bold**` or `__bold__`        | **bold**                    |
| Italic        | `*italic*` or `_italic_`        | *italic*                    |
| Bold + Italic | `***both***` or `___both___`    | ***both***                  |
| Strikethrough *(Ext.)* | `~~crossed out~~`      | ~~crossed out~~             |
| Highlight *(Ext.)*     | `==highlighted==`      | `highlighted` (if supported)|
| Subscript *(Ext.)*     | `H~2~0`                | H₂O                         |
| Superscript *(Ext.)*   | `x^2^`                 | x²                          |
| Emoji *(Ext.)*         | `:smile:`              | 😊                          |

> For **mid-word** styling, use asterisks: `as**teris**ks` → as**teris**ks

---

## Code

### Inline Code

```md
JS Variable: `let x = 1`
```

**Output:** JS Variable: `let x = 1`

---

### Code Block

````md
```js
const x = 3
let y = 4
```
````

```js
const x = 3
let y = 4
```

> Specifying a language (e.g., `js`, `python`, `bash`) enables **syntax highlighting** where supported.  
> Code blocks are technically extended Markdown but work almost everywhere.

