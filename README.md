# Corner Cup: Team Website Activity

Build a three-page website for **Corner Cup**, a fictional neighborhood café, as a team of three. You'll use **HTML and CSS only** (no JavaScript) and work together through **GitHub**.

Each of you builds one page. The header, footer and shared styles are already done, so all three of you can work at the same time without getting in each other's way.

## Your roles

| | You build | Your files (edit only these) | Your branch |
|---|---|---|---|
| Student 1 | Home page | `index.html`, `css/home.css` | `home-page` |
| Student 2 | Menu page | `menu.html`, `css/menu.css` | `menu-page` |
| Student 3 | Visit page | `visit.html`, `css/visit.css` | `visit-page` |

Already done, please don't edit: `css/base.css`, the header and footer in each page, and everything in `images/`.

## Project structure

```
corner-cup/
├── index.html        Student 1: Home
├── menu.html         Student 2: Menu
├── visit.html        Student 3: Visit
├── css/
│   ├── base.css      Shared styles (provided)
│   ├── home.css      Student 1
│   ├── menu.css      Student 2
│   └── visit.css     Student 3
└── images/           Illustrations and icons (provided)
```

## Timeline (about 100 minutes)

| Time | What you do |
|---|---|
| 10 min | Clone the repo, create your branch, open your page |
| 60 min | Build your page, committing after each TODO |
| 20 min | Open a pull request and review a teammate's |
| 10 min | Merge everything and test the whole site together |

## 1. Get set up

```bash
git clone <your-repo-url>
cd corner-cup
git checkout -b home-page      # Student 2: menu-page   Student 3: visit-page
```

Open your HTML file in your editor and in the browser. Your page already has the header and footer, and everything you build goes inside `<main>`.

Your HTML file and your CSS file both have numbered TODO comments. The HTML TODOs give you the exact text to use and suggested class names; the CSS TODOs give hints for styling. Work through them in order.

## 2. Team rules

1. **Only edit your own two files.** That way nobody gets a merge conflict.
2. **Use the shared variables** from `base.css` (like `var(--color-primary)` or `var(--space-4)`) instead of typing new colors and sizes. That's what makes three pages look like one website.
3. **Use the shared classes** where they fit: `.container`, `.section`, `.section-title`, `.section-intro`, `.button`, `.button--secondary` and `.page-header`.
4. **Need a change in `base.css`?** Ask your teacher instead of editing it.
5. **Commit after each TODO** with a short message that says what you added, for example `Add hero section`.

## 3. Team contracts

Your pages link to each other. A link to `page.html#something` only works if your teammate gives an element `id="something"`, so these ids are promises. Don't rename them.

| Link on | Goes to | Who adds the target |
|---|---|---|
| Home: "Book a table" button | `visit.html#contact` | Student 3: `id="contact"` on the contact section |
| Home: specials banner button | `menu.html#specials` | Student 2: `id="specials"` on the specials section |
| Menu: group-order note | `visit.html#contact` | Student 3 |
| Visit: intro paragraph | `index.html#why-us` | Student 1: `id="why-us"` on the features section |

## 4. Your task

Each table is your checklist: your page is done when every row is true. Stretch goals are optional, for if you finish early.

### Student 1: Home page

| Area | Requirement |
|---|---|
| Hero | Mint background. Heading, intro text and two buttons on the left; the storefront illustration on the right. |
| Hero links | "See the menu" goes to `menu.html`. "Book a table" goes to `visit.html#contact` and uses `.button--secondary`. |
| Images | The storefront has descriptive alt text. The three feature icons are decorative, so they use `alt=""`. |
| Feature cards | Three white cards in a 3-column grid with equal gaps. The section has `id="why-us"`. |
| Specials banner | A full-width marigold band with a heading, one line of text and a button to `menu.html#specials`. |
| Phone layout | At 700px and narrower, the hero stacks, the cards go to one column and the banner stacks. |
| Stretch | A customer quote built with `<figure>`, `<blockquote>` and `<figcaption>`. |

### Student 2: Menu page

| Area | Requirement |
|---|---|
| Page header | Uses the shared `.page-header` class, with an `<h1>` and an intro line. |
| Category links | A `<nav>` with links to `#specials`, `#coffee` and `#pastries`, styled as a row of pill-shaped links. |
| Specials | A section with `id="specials"` holding two cards. Each card has an image with alt text, a name, a price and a description. The cards sit side by side on wide screens. |
| Menu lists | Coffee (`id="coffee"`) and Pastries (`id="pastries"`) sections. Each is a `<ul>` of 4 items with the name and price on one line and the description below. |
| Layout | Menu items sit in two columns on wide screens, with a dashed line under each item. |
| Group note | A highlighted note at the bottom that links to `visit.html#contact`. |
| Phone layout | At 700px and narrower, the specials and menu items go to one column. |
| Stretch | "Bestseller" and "Vegan" badges on the items marked in the TODOs. |

### Student 3: Visit page

| Area | Requirement |
|---|---|
| Page header | Uses the shared `.page-header` class, with an `<h1>` and an intro that links to `index.html#why-us`. |
| Find us | The address inside an `<address>` element, plus the map image with descriptive alt text. |
| Opening hours | A `<table>` with a header row and a `<th scope="row">` for each day, with a line between rows. |
| Layout | "Find us" and "Opening hours" sit side by side as two white cards on wide screens. |
| Contact form | A section with `id="contact"` holding a form with name, email, visit date, number of guests (`<select>`), message (`<textarea>`) and a submit button. |
| Form accessibility | Every text field, the select and the textarea has a `<label>` connected with `for` and `id`. Name and email are `required`, and email uses `type="email"`. |
| Form styling | Fields fill their column, share the same border and rounded corners, and show a visible outline when focused. |
| Phone layout | At 700px and narrower, everything stacks into one column. |
| Stretch | A "What's this about?" radio group inside a `<fieldset>` with a `<legend>`, plus a newsletter checkbox. |

### Everyone: definition of done

- No sideways scrolling at 375px or 1280px wide (check with the device toolbar in your browser's DevTools).
- One `<h1>` on your page, and headings don't skip levels (h1, then h2, then h3).
- You can reach every link and form field with the Tab key and always see where you are.
- All your links work, including your team contracts.

## 5. Pull request and review

1. Push your branch: `git push -u origin home-page` (use your own branch name).
2. On GitHub, open a pull request from your branch into `main`. Give it a clear title, like "Home page".
3. Ask for a review, following this rotation: Student 1 reviews Student 2, Student 2 reviews Student 3, and Student 3 reviews Student 1.
4. **Reviewers:** check the pull request against the author's table above, at 375px and 1280px wide. Leave at least one thing that was done well and at least one thing to improve.
5. **Authors:** fix what's needed and push again (the pull request updates by itself), then merge once it's approved.

## 6. Test the whole site together

When all three pull requests are merged, everyone runs:

```bash
git checkout main
git pull
```

Open `index.html` and click through all three pages together. Every menu link and every team contract link should land in the right place.

## Shared design reference (`css/base.css`)

| Variable | Use it for |
|---|---|
| `--color-primary` | Buttons, links, prices |
| `--color-primary-dark` | Hover states, dark backgrounds |
| `--color-accent` | Marigold highlights (always put dark text on it) |
| `--color-accent-soft` | Badges and soft highlights |
| `--color-mint` | Soft green backgrounds |
| `--color-bg` | Page background |
| `--color-surface` | Cards and form fields (white) |
| `--color-text` | Main text |
| `--color-muted` | Secondary text |
| `--color-border` | Card borders and dividers |
| `--color-border-strong` | Form field borders |
| `--space-1` to `--space-8` | Spacing: 4, 8, 12, 16, 24, 32, 48 and 64px |
| `--radius-sm`, `--radius`, `--radius-lg`, `--radius-pill` | Rounded corners: 6px, 12px, 20px and fully round |
| `--shadow` | Soft card shadow |
| `--font-display` | Heading font (already applied to h1, h2 and h3) |

| Class | What it does |
|---|---|
| `.container` | Centers content and keeps it at most 1100px wide |
| `.section` | Adds vertical padding to a section |
| `.section-title` / `.section-intro` | Section heading and the muted line below it |
| `.button` | Green pill-shaped button (works on `<a>` and `<button>`) |
| `.button--secondary` | Outlined version; add it next to `.button` |
| `.page-header` | Mint title band for the top of the Menu and Visit pages |
