# Part 2 — Build the HTML skeleton

Open `index.html`. You will add one piece at a time.

---

## Step 1 — Tell the browser this is HTML5

Type:

```html
<!DOCTYPE html>
```

**What it does:** The doctype is the first line of every modern web page. It tells the browser: “Treat this as HTML5.” Without it, the browser may use old “quirks” rules and your layout can look wrong.

### Check yourself

- The very first line of the file is `<!DOCTYPE html>`  
- There is no space inside `DOCTYPE`  
- It is not closed with `</DOCTYPE>` — this line stands alone  

---

## Step 2 — Open the HTML document and set the language

On the next line, type:

```html
<html lang="en">
```

**What it does:**

- `<html>` is the root wrapper. Almost everything else sits inside it.
- `lang="en"` is an **attribute**. It says the page language is English. Screen readers and search engines use this.

You will close this tag at the very end with `</html>`.

---

## Step 3 — Start the head (information about the page)

```html
<head>
```

**What it does:** The `<head>` holds metadata: title, character set, and links to CSS. Visitors do **not** see the head as a box on the page. They see its effects (tab title, fonts, colors).

---

## Step 4 — Set the character encoding

Inside the head, indented with two spaces:

```html
  <meta charset="UTF-8">
```

**What it does:** `UTF-8` is a character set that can show English letters, the copyright symbol ©, and most world languages. Always put this near the top of `<head>`.

Notice: `<meta>` does not need a closing tag.

---

## Step 5 — Give the page a title (browser tab)

```html
  <title>UPSA IT Dept School</title>
```

**What it does:** Whatever you type between `<title>` and `</title>` appears on the browser tab and in bookmarks.

Try it later: change the words and refresh the browser. The tab text will change.

---

## Step 6 — Connect the CSS file

```html
  <link rel="stylesheet" href="style.css">
```

**What it does:**

- `rel="stylesheet"` means “this link is a style sheet.”
- `href="style.css"` is the path to your CSS file.

Because both files sit in the **same folder**, the name alone is enough. If you misspell `style.css` or put the file in another folder, the page will have no colors.

`<link>` also has no closing tag.

---

## Step 7 — Close the head

```html
</head>
```

Every opening tag that is not self-closing must be closed. Think of tags as boxes: you open a box, put things in, then close it.

### Check yourself — head is complete

Your file should look like this so far:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>UPSA IT Dept School</title>
  <link rel="stylesheet" href="style.css">
</head>
```

- [ ] `<head>` is closed  
- [ ] Title text is between the title tags  
- [ ] `href="style.css"` matches the CSS filename  

---

## Step 8 — Open the body (what people see)

```html
<body>
```

**What it does:** Everything the visitor sees—menu, heading, paragraph, footer—goes inside `<body>`.

---

## Step 9 — Add a header for the top of the page

```html
  <header>
```

**What it does:** `<header>` is a **semantic** tag. It does not look special by itself. It tells humans and browsers: “This is the top branding / navigation area.” You will style it blue later with CSS.

---

## Step 10 — Add a navigation menu

```html
    <nav>
```

**What it does:** `<nav>` marks a block of links used to move around the site.

---

## Step 11 — Start an unordered list

```html
      <ul>
```

**What it does:** `<ul>` means “unordered list.” Browsers draw bullet points by default. CSS will remove the bullets and line the items up in a row.

---

## Step 12 — Add the first menu item (a link)

```html
        <li><a href="#">Home</a></li>
```

**What each piece does:**

| Piece | Role |
|-------|------|
| `<li>` | One list item |
| `<a>` | A hyperlink (anchor) |
| `href="#"` | Where the link goes. `#` is a **placeholder**—it stays on this page |
| `Home` | The clickable text |
| `</a>` and `</li>` | Close the link, then close the list item |

Later you can change `href="#"` to a real file, for example `href="login.html"`.

---

## Step 13 — Add the rest of the menu

Type four more list items the same way:

```html
        <li><a href="#">Login Form</a></li>
        <li><a href="#">Contact Us</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Gallery</a></li>
```

**Practice idea:** Change “News” to your own name and see it appear in the menu after you open the page.

---

## Step 14 — Close the list, nav, and header

Close boxes in **reverse order** (last opened, first closed):

```html
      </ul>
    </nav>
  </header>
```

### Check yourself — header and menu

```html
  <header>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Login Form</a></li>
        <li><a href="#">Contact Us</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Gallery</a></li>
      </ul>
    </nav>
  </header>
```

- [ ] Five `<li>` items  
- [ ] Each `<a>` is inside an `<li>`  
- [ ] `</ul>`, `</nav>`, `</header>` are in that order  

---

## Step 15 — Add the main content

```html
  <main>
    <h1>Welcome to UPSA IT Dept School</h1>
    <p>This is a simple web application built with HTML and CSS.</p>
  </main>
```

**What it does:**

- `<main>` holds the unique content of this page (not the menu or footer).
- `<h1>` is the **biggest heading**. Use only one `<h1>` per page. Smaller headings are `<h2>` through `<h6>`.
- `<p>` is a paragraph of normal text.

### Check yourself

- [ ] One `<h1>`  
- [ ] Paragraph is inside `<main>`  
- [ ] `</main>` is present  

---

## Step 16 — Add a footer with copyright

```html
  <footer>
    <p>&copy; 2026 UPSA Communication Studies</p>
  </footer>
```

**What it does:**

- `<footer>` is the bottom strip of the page.
- `&copy;` is an **HTML entity**. The browser shows it as ©.  
  You cannot type a raw © and always trust it; entities are the safe way.

Other useful entities: `&amp;` → &, `&lt;` → <, `&nbsp;` → a space that will not collapse.

---

## Step 17 — Close the body and the HTML document

```html
</body>
</html>
```

Save the file (**Ctrl+S** or **Cmd+S**).

---

## Step 18 — Open the page in a browser

1. Go to your `upsa-it-webpage` folder.
2. Double-click `index.html`.  
   Or, in the browser: File → Open File → choose `index.html`.

**What you should see right now (before CSS):**

- A bullet list of five links at the top (underlined, usually blue)
- A large heading
- A paragraph
- A copyright line at the bottom

That “plain” look is normal. HTML is structure. CSS will dress it up.

### Check yourself

- [ ] Browser tab says **UPSA IT Dept School**  
- [ ] You see all five menu words  
- [ ] You see © 2026 (not the letters `&copy;`)  
- [ ] If you see `&copy;` as text, you typed it wrong (must be `&copy;`)  

---

# Part 1 complete — full `index.html`

Compare your file to this. Spacing can differ; tags and spelling must match.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>UPSA IT Dept School</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Login Form</a></li>
        <li><a href="#">Contact Us</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Gallery</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <h1>Welcome to UPSA IT Dept School</h1>
    <p>This is a simple web application built with HTML and CSS.</p>
  </main>
  <footer>
    <p>&copy; 2026 UPSA Communication Studies</p>
  </footer>
</body>
</html>
```

---
