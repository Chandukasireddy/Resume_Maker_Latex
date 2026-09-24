# Syntax & Escaping Rules

LaTeX uses special characters as syntax directives. Passing unescaped special characters directly into `.tex` files causes compilation failures or missing content.

---

## 1. Mandatory Reserved Character Escaping

Always escape the following 10 special characters in text content:

| Character | LaTeX Meaning | Correct Escaped Syntax | Common Error if Unescaped |
|---|---|---|---|
| `%` | Line comment | `\%` | Truncates the rest of the line silently |
| `&` | Alignment / Column separator | `\&` | `Misplaced alignment tab character &` |
| `$` | Math mode delimiter | `\$` | `Missing $ inserted` |
| `_` | Subscript operator | `\_` | `Missing $ inserted` |
| `#` | Macro parameter token | `\#` | `Illegal parameter number in definition` |
| `{` | Environment / Group start | `\{` | Missing bracket or syntax error |
| `}` | Environment / Group end | `\}` | Missing bracket or syntax error |
| `~` | Non-breaking space | `\textasciitilde{}` or `$\sim$` | Renders as non-breaking space |
| `^` | Superscript operator | `\textasciicircum{}` | `Missing $ inserted` |
| `\` | Escape character | `\textbackslash{}` | Starts an unintended macro command |

---

## 2. Common Escaping Scenarios in Resumes

### Percentages (Metrics & Gains)
- ❌ **Raw:** `95% precision gain`
- ❌ **Broken LaTeX:** `95% precision gain` *(everything after `%` is ignored as a comment)*
- ✅ **Correct LaTeX:** `\textbf{95\%} precision gain`

### Tech Stack & Tool Names
- ❌ **Raw:** `C# & C++ developer`
- ❌ **Broken LaTeX:** `C# & C++ developer` *(causes column alignment error)*
- ✅ **Correct LaTeX:** `C\# \& C++ developer`

### URLs & Email Addresses
- ❌ **Raw:** `https://example.com/user_profile`
- ❌ **Broken LaTeX:** `https://example.com/user_profile` *(subscript error on `_`)*
- ✅ **Correct LaTeX:** `\url{https://example.com/user\_profile}` or `href{...}{...}`

### Math / Range Expressions
- ❌ **Raw:** `5K+ requests/sec & $10K budget`
- ✅ **Correct LaTeX:** `5K+ requests/sec \& \textbf{\$10K} budget`

---

## 3. Punctuation & Quotes Rules

### Smart Quotation Marks
LaTeX requires opening backticks (`` ` ``) and closing single quotes (`'`) for proper typography:
- Double Quotes: `` ``double quotes'' `` (Renders as “double quotes”)
- Single Quotes: `` `single quotes' `` (Renders as ‘single quotes’)
- ❌ Do NOT use straight quotes `"text"`.

### Hyphens and Dashes
- **Hyphen (`-`):** Used for compound words (`full-stack`, `high-impact`).
- **En-dash (`--`):** Used for date and number ranges (`2022--2024`, `lines 15--25`).
- **Em-dash (`---`):** Used for parenthetical thoughts (`built a system---the first of its kind---in C++`).
