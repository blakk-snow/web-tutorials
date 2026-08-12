# Part 3 — Style the page with CSS

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















# Full `style.css`

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