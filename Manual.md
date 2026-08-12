# Create Your First Web Page  
## A Step-by-Step Tutoring Manual for Complete Beginners

**Project:** UPSA IT Dept School homepage  
**Skills you will learn:** HTML structure, CSS styling, how a browser reads files  
**Time:** about 45–60 minutes  
**What you need:** a computer, a text editor, and a web browser

This manual walks you from an empty folder to a finished, styled web page. Type every line yourself. Do not copy-paste if you can help it—typing is how the tags stick in your memory.

---

## How to use this manual

1. Do **one step at a time**.
2. After each step, look at the **Check yourself** box before moving on.
3. If something looks wrong, compare your file to the **full code** at the end of that part.
4. Words in `this style` are code. Type them exactly, including angle brackets `< >`.

**Tiny vocabulary**

| Word | Meaning |
|------|---------|
| HTML | The skeleton of a page (headings, paragraphs, links) |
| CSS | The clothes of a page (colors, spacing, layout) |
| Tag | A label like `<p>` that tells the browser what something is |
| Element | An opening tag, content, and a closing tag, e.g. `<p>Hello</p>` |
| Attribute | Extra info inside a tag, e.g. `lang="en"` |
| Browser | Chrome, Edge, Firefox, or Safari—the program that displays your page |

---

# Part 0 — Set up your workspace (5 minutes)

## Step 0.1 — Create a project folder

1. On your computer, open **Documents** (or Desktop).
2. Create a new folder named `upsa-it-webpage`.
3. Open that folder. You will put two files inside it.

## Step 0.2 — Choose a text editor

You need a plain-text editor, **not** Microsoft Word.

Good free choices:

- **VS Code** (recommended): https://code.visualstudio.com
- **Notepad++** (Windows)
- **TextEdit** on Mac: Format → Make Plain Text
- **Notepad** on Windows works, but has no color highlighting

Open your editor, then open the empty `upsa-it-webpage` folder.

## Step 0.3 — Create two empty files

In the folder, create:

1. `index.html` — the page content  
2. `style.css` — the look and feel  

Names must match exactly (all lowercase). The browser and the `<link>` tag depend on this.

### Check yourself

- [ ] Folder `upsa-it-webpage` exists  
- [ ] It contains `index.html` and `style.css`  
- [ ] Both files are empty for now  

---

# Part 1 — Build the HTML skeleton

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

# Part 2 — Style the page with CSS

Open `style.css`. CSS works in **rules**:

```css
selector {
  property: value;
}
```

- **Selector** = which HTML element to style (`body`, `header`, `nav a`, …)  
- **Property** = what to change (`color`, `padding`, …)  
- **Value** = how to change it (`white`, `20px`, …)

Each property line ends with a **semicolon** `;`. Forgetting it is the most common beginner bug.

After every step, **save `style.css`**, then **refresh** the browser (F5).

---

## Step 19 — Style the whole page (`body`)

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}
```

**What it does:**

- `font-family: Arial, sans-serif;`  
  Use Arial if the computer has it. If not, use any generic sans-serif font (letters without little “feet”).
- `margin: 0;` and `padding: 0;`  
  Browsers add default space around the page. Setting both to 0 gives you a clean slate so the blue header can touch the edges of the window.

**Margin vs padding (remember this):**

- **Margin** = space **outside** a box  
- **Padding** = space **inside** a box  

### Check yourself

- [ ] Refresh: the page text should look like Arial  
- [ ] The extra white gap at the very edge of the window should shrink  

---

## Step 20 — Style the header (dark blue bar)

```css
header {
  background: #004080;
  color: white;
  padding: 10px 0;
}
```

**What it does:**

- `background: #004080;` — a dark blue.  
  `#004080` is a **hex color**: `#` + red + green + blue in hexadecimal. `00` red, `40` green, `80` blue.
- `color: white;` — text inside the header is white (so it shows on blue).
- `padding: 10px 0;` — two numbers mean **top/bottom** then **left/right**.  
  10 pixels of space above and below the menu; 0 extra space on the sides.

### Check yourself

- [ ] A blue bar appears across the top  
- [ ] Menu text is white (links may still be underlined until the next steps)  

**Experiment:** Change `#004080` to `#800000` (dark red), save, refresh. Change it back when you understand hex colors.

---

## Step 21 — Turn the bullet list into a horizontal menu

```css
nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 20px;
}
```

**What it does:**

- `nav ul` means “the `<ul>` that sits inside `<nav>`.” This is a **descendant selector**. It will not change other lists you might add later.
- `list-style: none;` — remove bullets.
- `display: flex;` — put children in a row (a flexible box).
- `justify-content: center;` — center that row in the header.
- `gap: 20px;` — 20 pixels of space between items.

### Check yourself

- [ ] No bullets  
- [ ] Home, Login Form, Contact Us, News, Gallery sit in one centered row  

---

## Step 22 — Style the links

```css
nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}
```

**What it does:**

- `nav a` = every `<a>` inside `<nav>`.
- `color: white;` — override the browser’s default blue link color.
- `text-decoration: none;` — remove the underline.
- `font-weight: bold;` — thicker text, easier to tap and read.

### Check yourself

- [ ] Menu looks like white bold words, no underline  
- [ ] Hovering may still show a hand cursor (that is normal)  

---

## Step 23 — Style the main content

```css
main {
  padding: 20px;
  text-align: center;
}
```

**What it does:**

- `padding: 20px;` — breathing room on all four sides so text is not glued to the header or the window edge.
- `text-align: center;` — center the heading and paragraph.

### Check yourself

- [ ] Welcome heading and paragraph are centered  
- [ ] There is space between the blue bar and the heading  

---

## Step 24 — Style the footer

```css
footer {
  background: #eee;
  text-align: center;
  padding: 10px;
}
```

**What it does:**

- `background: #eee;` — light gray. Short hex: `#eee` is the same as `#eeeeee`.
- `text-align: center;` — center the copyright line.
- `padding: 10px;` — space inside the gray bar.

### Check yourself

- [ ] A light gray strip at the bottom  
- [ ] © 2026 UPSA Communication Studies is centered  

---

# Part 2 complete — full `style.css`

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background: #004080;
  color: white;
  padding: 10px 0;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 20px;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

main {
  padding: 20px;
  text-align: center;
}

footer {
  background: #eee;
  text-align: center;
  padding: 10px;
}
```

Save both files and refresh. You should see a clean, simple, professional school homepage.

---

# Part 3 — Extra credit (optional)

Do these only after Parts 1 and 2 work.

## Step 25 — Hover effect on menu links

Add this **after** the `nav a` rule:

```css
nav a:hover {
  color: #ffcc00;
  text-decoration: underline;
}
```

**What it does:** `:hover` is a **pseudo-class**. It applies only while the mouse is over the link. Gold text plus an underline makes the menu feel clickable.

Refresh and move your mouse across the menu.

---

## Step 26 — Point a link at a real page (preview of multi-page sites)

1. Create a new file `contact.html` in the same folder.
2. Put a tiny page in it:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contact Us</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="#">Login Form</a></li>
        <li><a href="contact.html">Contact Us</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Gallery</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <h1>Contact Us</h1>
    <p>Email the IT department at it@upsa.edu.gh</p>
  </main>
  <footer>
    <p>&copy; 2026 UPSA Communication Studies</p>
  </footer>
</body>
</html>
```

3. In `index.html`, change only the Contact link:

```html
<li><a href="contact.html">Contact Us</a></li>
```

Open `index.html`, click **Contact Us**. You should land on the new page. Click **Home** to come back.

---

# Troubleshooting (when something looks broken)

| Problem | Likely cause | Fix |
|---------|--------------|-----|
| No colors / page looks like Step 18 | CSS not linked | Check `<link rel="stylesheet" href="style.css">` and that both files are in the same folder |
| Tab title is the filename | Missing or empty `<title>` | Add `<title>UPSA IT Dept School</title>` inside `<head>` |
| You see `&copy;` on the page | Entity typed wrong | Must be exactly `&copy;` |
| Menu still has bullets | CSS typo in `nav ul` | Check `list-style: none;` and the semicolon |
| Menu is a vertical stack | `display: flex;` missing or misspelled | Fix the `nav ul` rule |
| Blue header only behind the words, not full width | You set width by mistake, or header is not a block | Do not add `width` yet; `header` should be full width by default |
| Changes do not appear | File not saved, or old tab cached | Save, then hard refresh: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac) |
| Half the page missing | Unclosed tag | Count opening vs closing tags; use the full HTML listing above |
| CSS does nothing for one rule | Missing `}` or `;` | Look at the rule above the one that failed |

**How to “see” errors:** In the browser, right-click the page → **Inspect** → **Console**. Red messages often mean a missing file (wrong `href`).

---

# What you learned (keep this list)

1. A web page is files on disk. The browser reads them; it does not need the internet for this project.  
2. HTML describes **meaning**: header, nav, main, footer, headings, links.  
3. Tags come in pairs (except a few like `<meta>` and `<link>`).  
4. Attributes add details: `lang`, `href`, `rel`, `charset`.  
5. CSS selects elements and sets properties.  
6. Hex codes like `#004080` are colors.  
7. Flexbox (`display: flex`) lines items up in a row.  
8. Semantic tags make the page easier to style and easier for screen readers.

---

# Practice challenges (do these on your own)

1. Change the heading to include **your name**.  
2. Change the header color to your school’s color. Look up a hex code.  
3. Add a sixth menu item called **About**.  
4. Add a second paragraph under the welcome text.  
5. Make the footer background `#004080` and the footer text white.  
6. Add a hover rule so links become yellow (Step 25).  
7. Create `news.html` and link **News** to it the same way as Contact.

---

# Teacher / parent notes

- Expected finished look: full-width navy header, centered white menu, centered welcome text, light gray footer.  
- If the learner is stuck, have them read tags **out loud** (“open header, open nav…”). Mismatched closes become obvious.  
- Resist adding JavaScript until this page is built from memory once.  
- Next natural lessons: more pages, images (`<img src="" alt="">`), a simple contact form, and mobile layout with a media query.

You built a real web page from nothing. Save the folder. That is your first site.
