

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
