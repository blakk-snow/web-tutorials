
# Part 4 — Extra credit (optional)

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
