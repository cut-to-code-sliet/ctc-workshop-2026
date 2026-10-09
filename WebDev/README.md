# CTC Web Development Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: Web Basics, Terminal Commands & HTML/CSS Intro (21 Sep 2026)](#session-1-web-basics-terminal-commands--htmlcss-intro-21-sep-2026)
- [Session 2: Homework Recap & Building the YouTube Topbar with Flexbox](#session-2-homework-recap--building-the-youtube-topbar-with-flexbox)
- [Session 3: Building the Sidebar, Selectors & Hover Effects](#session-3-building-the-sidebar-selectors--hover-effects)
- [Session 4: Positioning, Code Review & Putting the Page Together](#session-4-positioning-code-review--putting-the-page-together)

---

## Session 1: Web Basics, Terminal Commands & HTML/CSS Intro (21 Sep 2026)

### Topics Covered

#### 1. How the Web Works: Frontend, Backend & Database
- **Frontend**: everything the user sees and interacts with in the browser (layout, colors, buttons, text, images). Built with **HTML** (structure), **CSS** (styling) and **JavaScript** (behavior).
- **Backend**: the server-side logic that runs behind the scenes. It handles requests, business logic, authentication and talks to the database. (Languages/tools: Node.js, Python, Java, PHP, etc.)
- **Database (DB)**: where data is stored permanently (users, posts, orders). Backend reads from and writes to it. (Examples: MySQL, PostgreSQL, MongoDB.)
- **How they connect**: the browser (client) sends a **request** → the backend (server) processes it and queries the DB → the server sends back a **response** → the browser displays it.

```
Browser (Frontend)  ──request──▶  Server (Backend)  ──query──▶  Database
Browser (Frontend)  ◀─response──  Server (Backend)  ◀─data────  Database
```

#### 2. Basic Terminal Commands
The terminal lets you control your computer by typing commands instead of clicking. You will use it constantly for web dev (running servers, git, npm, etc.).

| Command | What it does | Example |
|---------|--------------|---------|
| `pwd` | Print working directory (where am I?) | `pwd` |
| `ls` | List files and folders in the current directory | `ls`, `ls -l`, `ls -a` |
| `cd <folder>` | Change directory (go into a folder) | `cd projects` |
| `cd ..` | Go one level up (to the parent folder) | `cd ..` |
| `mkdir <name>` | Make a new directory | `mkdir my-website` |

**More basic commands worth knowing:**

| Command | What it does | Example |
|---------|--------------|---------|
| `cd` (alone) / `cd ~` | Go to your home directory | `cd ~` |
| `touch <file>` | Create an empty file (macOS/Linux/Git Bash) | `touch index.html` |
| `cp <src> <dest>` | Copy a file | `cp index.html backup.html` |
| `mv <src> <dest>` | Move or rename a file | `mv old.html new.html` |
| `rm <file>` | Delete a file (**permanent, no recycle bin!**) | `rm test.html` |
| `rm -r <folder>` | Delete a folder and everything inside it | `rm -r old-project` |
| `rmdir <folder>` | Delete an *empty* folder | `rmdir empty-folder` |
| `cat <file>` | Print the contents of a file | `cat index.html` |
| `echo "text"` | Print text (or write it to a file with `>`) | `echo "Hello" > hi.txt` |
| `clear` | Clear the terminal screen | `clear` |
| `whoami` | Show the current user | `whoami` |
| `code .` | Open the current folder in VS Code | `code .` |
| `man <cmd>` / `<cmd> --help` | Show help for a command | `ls --help` |

> **Windows users:** In PowerShell/CMD, some names differ: `dir` instead of `ls`, `cd` (alone) to print the current path instead of `pwd`, `type` instead of `cat`, `del` instead of `rm`, `cls` instead of `clear`. Installing **Git Bash** or **WSL** gives you the Linux-style commands above.

**Tips:**
- Press `Tab` to auto-complete file and folder names.
- Press the `↑` arrow to bring back previous commands.
- Folder names with spaces need quotes: `cd "my folder"`.

#### 3. Introduction to HTML & CSS
- **HTML (HyperText Markup Language)** gives a web page its **structure and content**.
- **CSS (Cascading Style Sheets)** controls how it **looks** (colors, spacing, fonts, layout).

**Basic structure of an HTML document**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is my first web page.</p>
  </body>
</html>
```

- **`<!DOCTYPE html>`**: tells the browser this is an HTML5 document.
- **`<html>`**: the root element that wraps everything.
- **`<head>`**: metadata *about* the page (title, character set, linked CSS). Not displayed on the page itself.
- **`<body>`**: everything the user actually sees.

#### 4. Tags and Attributes
- **Tag**: the building block of HTML, usually written as an opening tag and a closing tag around content: `<p>Some text</p>`
- **Element**: the full thing: opening tag + content + closing tag.
- **Self-closing (void) tags** have no closing tag, e.g. `<img />`, `<br />`.
- **Attribute**: extra information written inside the opening tag as `name="value"`.

```html
<a href="https://developer.mozilla.org" class="link">Visit MDN</a>
<!--  ↑ tag   ↑ attribute (href)                ↑ content -->
```

#### 5. Block, Inline & Inline-Block Elements

| Type | Starts on a new line? | Width/Height can be set? | Examples |
|------|-----------------------|--------------------------|----------|
| **Block** | Yes, takes the full available width | Yes | `<div>`, `<p>`, `<h1>`–`<h6>`, `<ul>` |
| **Inline** | No, flows with the text | No (ignored) | `<span>`, `<a>`, `<strong>`, `<em>` |
| **Inline-block** | No, sits in the line like inline | Yes | `<button>`, `<img>` (by default), or anything with `display: inline-block` |

```css
span   { display: block; }         /* make an inline element behave like block */
div    { display: inline; }        /* make a block element behave like inline */
a      { display: inline-block; }  /* flows inline, but accepts width/height */
```

#### 6. Common Tags

| Tag | Purpose | Example |
|-----|---------|---------|
| `<title>` | Page title shown in the browser tab (goes in `<head>`) | `<title>My Site</title>` |
| `<p>` | Paragraph of text | `<p>Hello there</p>` |
| `<a>` | Anchor / link to another page or resource | `<a href="https://google.com">Google</a>` |
| `<button>` | Clickable button | `<button>Click me</button>` |
| `<img>` | Displays an image (self-closing) | `<img src="cat.png" alt="A cat" />` |

#### 7. Common Attributes

| Attribute | Used for | Example |
|-----------|----------|---------|
| `href` | Destination URL of a link (used on `<a>`) | `<a href="https://google.com">Go</a>` |
| `class` | Gives an element a name so CSS can style it (many elements can share one class) | `<p class="intro">Hi</p>` |
| `color` | Note: `color` is a **CSS property**, not an HTML attribute. It sets text color. | `p { color: red; }` |
| `src` / `alt` | Image source and alternative text (for `<img>`) | `<img src="a.png" alt="Logo" />` |

**Using `class` and `color` together:**

```html
<style>
  .intro {
    color: teal;
  }
</style>

<p class="intro">This text is teal.</p>
```

---

### Resources

- **Frontend, Backend & Databases**
  - [Server-side Website Programming: First Steps (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps)
  - [Client-Server Overview (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Client-Server_overview)
  - [What is a Web Server? (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server)
- **Terminal / Command Line**
  - [Command Line Crash Course (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line)
  - [GNU Coreutils Manual (docs for `ls`, `cp`, `mv`, `rm`, `cat`, `mkdir`, `pwd`, etc.)](https://www.gnu.org/software/coreutils/manual/coreutils.html)
- **HTML Document Structure**
  - [HTML Basics (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)
  - [Doctype (MDN Glossary)](https://developer.mozilla.org/en-US/docs/Glossary/Doctype)
  - [`<head>` element (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)
  - [`<body>` element (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)
- **Tags & Attributes**
  - [HTML Elements Reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
  - [HTML Attributes Reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
  - [Global Attribute: `class` (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class)
- **Block, Inline & Inline-Block**
  - [Block-level Content (MDN)](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content)
  - [Inline-level Content (MDN)](https://developer.mozilla.org/en-US/docs/Glossary/Inline-level_content)
  - [CSS `display` property (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- **Common Tags**
  - [`<a>` Anchor (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
  - [`<p>` Paragraph (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)
  - [`<button>` (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button)
  - [`<img>` Image (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img)
  - [`<title>` (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
- **CSS Basics**
  - [CSS `color` property (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
  - [CSS First Steps (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps)
- **For the homework**
  - [The Box Model (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
  - [CSS `margin` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
  - [CSS `padding` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
  - [CSS `border-radius` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

---

### Practice Questions
1. In your own words, explain what the frontend, backend and database do when you log in to a website.
2. Using only the terminal, create a folder called `my-website`, go inside it, create a file `index.html`, and then come back to the parent folder.
3. Write the basic HTML skeleton (`doctype`, `html`, `head`, `body`) from memory and set the page title to your name.
4. Create a page with two `<span>` elements and two `<p>` elements. Observe how they are laid out, then change their `display` values and see what happens.
5. Add a link (`<a>`), an image (`<img>`) and a `<button>` to your page. Give the link a `class` and style its `color` using CSS.

### Homework
1. What is the **anchor tag (`<a>`)**? (Covered in class, so revise your notes and the [MDN page](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a).)
2. What would be the **ratio of height and width** to make a button circle-shaped? *(Hint: a circle is a special case of a rounded shape. Think about which CSS property rounds corners, and what has to be true about the button's dimensions.)*
3. Learn about **margin and padding**. *(Hint: read about the CSS box model, and note where each one adds space: inside or outside the border.)*

---

## Session 2: Homework Recap & Building the YouTube Topbar with Flexbox

**Goal of this session:** revise the Session 1 homework, then start our first mini-project, a **YouTube clone**. Today we build the **topbar** (hamburger menu, logo, search bar, and icons on the right).

### Topics Covered

#### 1. Homework Recap (Answers)

**1. The anchor tag `<a>`**
- Creates a **hyperlink** to another page, file, email address, or a spot on the same page.
- The `href` attribute holds the destination.
- It is an **inline** element, so it flows with the text.

```html
<a href="https://developer.mozilla.org" target="_blank">Open MDN in a new tab</a>
```

**2. Circle-shaped button: what ratio?**
- Width : Height must be **1 : 1** (a perfect square), and then `border-radius: 50%` turns the square into a circle.
- If the sides are not equal, you get an oval/ellipse instead.

```css
.circle-btn {
  width: 50px;
  height: 50px;          /* same as width -> ratio 1:1 */
  border-radius: 50%;    /* round the corners fully */
}
```

**3. Margin vs Padding**

| | Margin | Padding |
|---|---|---|
| Where is the space? | **Outside** the border | **Inside** the border |
| Purpose | Pushes *other* elements away | Gives the content breathing room |
| Background color shows in it? | No (transparent) | Yes |
| Can be negative? | Yes | No |

```
┌──────────────── margin ────────────────┐
│  ┌────────────── border ────────────┐  │
│  │  ┌────────── padding ─────────┐  │  │
│  │  │         content            │  │  │
│  │  └────────────────────────────┘  │  │
│  └──────────────────────────────────┘  │
└────────────────────────────────────────┘
```

#### 2. Project Setup: Linking CSS to HTML
Keep your project in one folder with all assets next to the HTML file:

```
youtube-clone/
├── topbar.html
├── top.css
├── hamburger-menu.svg
├── youtube-logo.svg
├── search.svg
├── create.svg
├── youtube-apps.svg
├── notifications.svg
└── my-channel.jpeg
```

Connect the stylesheet inside `<head>` with a `<link>` tag:

```html
<link rel="stylesheet" href="top.css">
```

- `rel="stylesheet"` tells the browser *what* the linked file is.
- `href="top.css"` is the **relative path** to the file (same folder).
- If the style doesn't apply, check the file name and path first. This is the #1 beginner bug.

#### 3. Planning the Layout Before Coding
Always break a design into **boxes** first. The topbar has three parts:

```
┌───────────────────────────────────────────────────────────────┐
│  LEFT              │        MIDDLE              │   RIGHT     │
│  ☰  YouTube logo   │  [ search........ ] [🔍]   │ ＋ ▦ 🔔 👤  │
└───────────────────────────────────────────────────────────────┘
```

So the HTML is a `div.topbar` containing three child `div`s: `.left`, `.middle`, `.right`.

#### 4. The HTML of the Topbar

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>topbar</title>
    <link rel="stylesheet" href="top.css">
</head>
<body>
    <div class="topbar">
        <div class="left">
            <img class="hamburger-menu" src="hamburger-menu.svg" alt="">
            <img class="youtube-logo" src="youtube-logo.svg" alt="">
        </div>
        <div class="middle">
            <div class="search">
                <input type="text" placeholder="search">
            </div>
            <div class="searchicon">
                <img class="s" src="search.svg" alt="">
            </div>
            <div class="mic"></div>
        </div>
        <div class="right">
            <img src="create.svg" alt="">
            <img src="youtube-apps.svg" alt="">
            <img src="notifications.svg" alt="">
            <img src="my-channel.jpeg" alt="">
        </div>
    </div>
</body>
</html>
```

**Things to notice:**
- `<div>` is a **container** with no meaning of its own. We use it to group things.
- `<img>` is self-closing and needs `src` (where the image is) and `alt` (text description for accessibility/screen readers). Here `alt=""` marks the images as decorative. For meaningful images, write real text like `alt="YouTube logo"`.
- `<input type="text" placeholder="search">` creates a text box. `placeholder` is the grey hint text that disappears when you type.
- The `class` names (`left`, `middle`, `right`, `s`...) are the "handles" CSS uses to find elements.
- `.mic` is an empty placeholder box for a microphone icon we can add later.

#### 5. Flexbox: The Most Important Layout Tool
By default, `div`s are **block** elements and stack **vertically**. To put things **side by side**, make the parent a **flex container**:

```css
.topbar {
  display: flex;   /* children now sit in a row */
}
```

| Property | What it does | Values |
|----------|--------------|--------|
| `display: flex` | Turns an element into a flex container; its **direct children** become flex items | |
| `flex-direction` | Direction of the main axis | `row` (default), `column` |
| `justify-content` | Aligns items along the **main** axis | `flex-start`, `center`, `space-between`, `flex-end` |
| `align-items` | Aligns items along the **cross** axis | `stretch`, `center`, `flex-start`, `flex-end` |

> **Key idea:** `display: flex` only affects the **direct children**. Grandchildren are not affected unless their own parent is also flex. That's why `.left` and `.middle` each need their own `display: flex`.

#### 6. The CSS of the Topbar (Walkthrough)

```css
.topbar {
    display: flex;            /* left, middle, right sit side by side */
}

.hamburger-menu {
    width: 15px;              /* shrink the big SVG down */
}

.youtube-logo {
    width: 50px;
    margin-left: 15px;        /* gap between hamburger and logo */
}

.left {
    display: flex;            /* hamburger + logo in a row */
    flex-direction: row;
}

.middle {
    margin-left: 25px;        /* space between logo area and search bar */
    display: flex;            /* input + search button in a row */
}

input {
    border-radius: 1px;
    border: 0.5px solid grey; /* thin grey outline like YouTube's */
}

input::placeholder {
    font-size: 10px;          /* smaller hint text */
}

.s {
    border: 0.5px solid grey;
    width: 17.5px;
    margin-left: -0.5px;      /* overlap borders so there's no double line */
    background-color: rgb(207, 206, 206);
    margin-top: 0.5px;
}
```

**Line-by-line ideas to remember:**
- **Class selector** `.name { }` targets every element with `class="name"`.
- **Element selector** `input { }` targets *all* `<input>` elements on the page.
- **`::placeholder`** is a **pseudo-element**: it styles a special part of an element (the hint text).
- **`border: 0.5px solid grey`** is shorthand for `border-width border-style border-color`.
- **`rgb(207, 206, 206)`** mixes Red, Green, Blue (each 0-255). Equal values give greys.
- **Negative margin** (`margin-left: -0.5px`) pulls an element *toward* its neighbour. Handy, but use sparingly.
- **`width` on `<img>`:** when you set only width, the height scales automatically and keeps the picture's proportions.

#### 7. Units Quick Reference

| Unit | Meaning | Use when |
|------|---------|----------|
| `px` | Fixed pixels | Borders, small fixed sizes |
| `%` | Percentage of the parent | Flexible widths |
| `rem` | Multiple of the root font size (usually 16px) | Scalable text/spacing |
| `vw` / `vh` | 1% of viewport width/height | Full-screen layouts |

### Resources
- [Flexbox Basic Concepts (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox)
- [CSS `flex-direction` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)
- [CSS `::placeholder` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/::placeholder)
- [`<input>` element (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
- [`<link>` element (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link)
- [CSS `border` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
- [CSS Values and Units (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
- [Flexbox Froggy (game to practice flexbox)](https://flexboxfroggy.com/)

### Practice Questions
1. What is the difference between `margin` and `padding`? Draw the box model from memory.
2. Why do we write `alt` on every `<img>`? What value should a purely decorative image have?
3. Remove `display: flex` from `.topbar` in your project. What happens to the three sections, and why?
4. `.left` already sits inside a flex container. Why does it *also* need `display: flex` for the hamburger and logo to align in a row?
5. Make the search `<input>` wider and give it rounded corners on the left side only (hint: look up `border-top-left-radius`).

### Homework
1. Build the topbar from scratch **without copy-pasting**. Use your own images or icons from a free SVG site.
2. Add a microphone icon inside the `.mic` div and style it as a **circle** (remember the 1:1 ratio and `border-radius: 50%`).
3. Read about **`justify-content`** and **`align-items`** and try all values on `.topbar`. Take a screenshot of each and note what changes.
4. **Think about it:** in the topbar, the icons on the right are pushed to the far edge of the screen. How could you do that? (We'll look at it next session.)

---

## Session 3: Building the Sidebar, Selectors & Hover Effects

**Goal of this session:** build the YouTube **sidebar** (Home, Explore, Subscriptions, Originals, YouTube Music), learn how to **group selectors**, use **descendant selectors**, and add an interactive **`:hover`** effect.

### Topics Covered

#### 1. Homework Check
- Share your topbar and compare approaches.
- Common problem: *"My CSS isn't working."* Checklist:
  1. Is the CSS file linked with the right path?
  2. Does the class name in HTML match the CSS **exactly**? (Spelling and case matter.)
  3. Did you forget the dot (`.`) before a class selector?
  4. Is there a missing `;` or `}` earlier in the CSS file? One mistake can break everything below it.
- Use **browser DevTools** (`F12` or right-click → *Inspect*) to see which CSS rules apply to an element.

#### 2. Planning the Sidebar
Each sidebar item is an **icon on top** and a **small label below**. Every item has the same structure, so we repeat the pattern:

```
 ┌─────────┐
 │  [icon] │   ← <img>
 │  Home   │   ← <p>
 └─────────┘
```

The full sidebar is a vertical stack of 5 such items.

#### 3. The HTML of the Sidebar

```html
<div class="sidebar">
    <div class="home">
        <img src="home.svg" alt="">
        <p>Home</p>
    </div>
    <div class="explore">
        <img src="explore.svg" alt="">
        <p>Explore</p>
    </div>
    <div class="subs">
        <img src="subscriptions.svg" alt="">
        <p>Subscriptions</p>
    </div>
    <div class="ori">
        <img src="originals.svg" alt="">
        <p>Originals</p>
    </div>
    <div class="ytm">
        <img src="youtube-music.svg" alt="">
        <p>YouTube Music</p>
    </div>
</div>
```

> **Note:** this is a **fragment**. When you put it in a real page, it goes inside `<body>` of a full HTML document (with `<!DOCTYPE html>`, `<head>` and the `<link>` to the CSS). Always make sure every opening tag has its closing tag.

**Why one `div` per item?** Wrapping `img` + `p` together lets us treat each item as **one unit** (one box to hover over, one box to align).

#### 4. Flex Column & Centering

```css
.sidebar {
    margin-top: 5px;
    display: flex;
    flex-direction: column;   /* stack the 5 items vertically */
    width: 50px;              /* a narrow strip, like YouTube's mini sidebar */
}

.home, .explore, .subs, .ori, .ytm {
    display: flex;
    flex-direction: column;   /* icon above label */
    align-items: center;      /* center both horizontally */
    margin-left: -7px;        /* nudge the items left to look balanced */
}
```

**Remember the axes:**
- With `flex-direction: row`: main axis = horizontal, cross axis = vertical.
- With `flex-direction: column`: main axis = **vertical**, cross axis = **horizontal**.
- `align-items: center` works on the **cross axis**. With `column`, that means it **centers horizontally**.

#### 5. Grouping Selectors with a Comma
Instead of writing the same rules five times, **list the selectors separated by commas**:

```css
.home, .explore, .subs, .ori, .ytm {
    /* rules applied to ALL five */
}
```

This follows the **DRY principle**: *Don't Repeat Yourself*.

> **Better idea:** give all five items one shared class, like `class="item"`, and write `.item { ... }` once. (Try it for homework!)

#### 6. Descendant Selectors
A **space** between two selectors means "find the second **inside** the first":

```css
.sidebar img {        /* only <img> elements inside .sidebar */
    margin-top: 5px;
    width: 25px;
    margin-bottom: 2px;
}

.sidebar p {          /* only <p> elements inside .sidebar */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 7px;
}
```

Why not just `img { }`? Because that would also resize the topbar icons and everything else on the page. **Descendant selectors keep your styles scoped.**

| Selector | Meaning |
|----------|---------|
| `.a .b` | `.b` anywhere **inside** `.a` (descendant) |
| `.a, .b` | Both `.a` **and** `.b` (grouping) |
| `.a.b` | An element that has **both** classes |
| `.a > .b` | `.b` that is a **direct child** of `.a` |

#### 7. Typography Basics

```css
font-family: Arial, Helvetica, sans-serif;
```
- This is a **font stack**: the browser tries Arial first, then Helvetica, and finally *any* sans-serif font. The last one is the safety net.
- `font-size: 7px` sets the text size. (Quite small! Real sites use larger sizes for readability, so use `px` here only because we are matching a design.)
- Other useful properties: `font-weight`, `text-align`, `line-height`, `letter-spacing`.

#### 8. Hover Effects with `:hover`
A **pseudo-class** applies styles when the element is in a special **state**. `:hover` is active while the mouse pointer is over the element.

```css
.home:hover, .explore:hover, .subs:hover, .ori:hover, .ytm:hover {
    background-color: rgb(225, 224, 224);   /* light grey highlight */
}
```

Other common pseudo-classes: `:active` (while clicking), `:focus` (selected input), `:first-child`, `:last-child`.

**Make it feel smoother:**

```css
.home, .explore, .subs, .ori, .ytm {
    transition: background-color 0.2s ease;
    cursor: pointer;
}
```
- `transition` animates the change instead of snapping.
- `cursor: pointer` shows the hand icon, signalling "clickable."

#### 9. Colors in CSS

| Format | Example | Notes |
|--------|---------|-------|
| Name | `red`, `teal` | Easy but limited |
| HEX | `#e1e0e0` | Most common in design tools |
| RGB | `rgb(225, 224, 224)` | Red, Green, Blue (0-255) |
| RGBA | `rgba(0, 0, 0, 0.5)` | Adds transparency (0 to 1) |
| HSL | `hsl(0, 0%, 88%)` | Hue, Saturation, Lightness |

#### 10. The Topbar Gets a Look
In the combined stylesheet we also style the topbar itself:

```css
.topbar {
    display: flex;
    flex-direction: row;
    height: 40px;               /* fixed height for the bar */
    background-color: red;      /* a bright color is useful while testing layouts */
}

.left {
    display: flex;
    flex-direction: row;
    margin-left: 13px;
}
```

**Tip:** temporary bright backgrounds (`background-color: red;`) or outlines (`outline: 1px solid blue;`) are a great debugging trick to *see* where each box starts and ends.

### Resources
- [CSS Selectors (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)
- [Combinators (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators)
- [Pseudo-classes (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
- [CSS `:hover` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)
- [CSS `align-items` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)
- [CSS `transition` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)
- [Fundamental Text and Font Styling (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)
- [Chrome DevTools Overview](https://developer.chrome.com/docs/devtools/overview)

### Practice Questions
1. What is the difference between `.a .b`, `.a, .b` and `.a.b`?
2. In a `flex-direction: column` container, which axis does `align-items` control?
3. Why do we write `.sidebar img` instead of just `img`?
4. Add `transition` and `cursor: pointer` to the sidebar items and describe the difference you see.
5. Open DevTools, hover over a sidebar item and find the `:hover` rule in the Styles panel. (Tip: use the `:hov` button to force the state.)

### Homework
1. **Refactor:** give all five sidebar items a shared class `item` and delete the long comma-separated lists. The page should look identical.
2. Add two more sidebar items (e.g. *Library* and *History*).
3. Change the hover color to a different shade and add a thin **left border** on hover (hint: `border-left`).
4. Read about **`position: absolute`**, **`relative`**, **`fixed`** and **`sticky`**. We will use them next session.

---

## Session 4: Positioning, Code Review & Putting the Page Together

**Goal of this session:** understand **`position`**, review the code we wrote in Sessions 2 and 3 (find the bugs and "hacks"), clean it up, and combine the topbar and sidebar into **one complete page**.

### Topics Covered

#### 1. The `position` Property
By default every element has `position: static` and follows the normal flow of the page. `position` lets us break out of it.

| Value | Behavior |
|-------|----------|
| `static` | Default. Normal flow. `top/left/right/bottom` are ignored. |
| `relative` | Stays in the flow, but can be nudged from its *original* spot. Also becomes the reference point for absolute children. |
| `absolute` | Removed from the flow. Positioned relative to the **nearest positioned ancestor** (or the page if there isn't one). |
| `fixed` | Positioned relative to the **browser window**. Stays in place while scrolling. |
| `sticky` | Behaves like `relative` until you scroll to a threshold, then sticks like `fixed`. |

**Example:** the right-hand icons in our topbar:

```css
.right {
    display: flex;
    position: absolute;   /* take it out of the normal flow */
    right: 0;             /* glue it to the right edge */
    margin-top: -15px;    /* manual adjustment to line it up */
}
```

- `position: absolute; right: 0;` pins the icon group to the right edge of the page.
- Because the element is out of the flow, the other sections no longer "know" it exists, which is why a manual `margin-top: -15px` was needed to fix the vertical alignment. That is a **hack**.

#### 2. A Cleaner Way: `justify-content: space-between`
Since `.topbar` is already a flex container, we can **avoid absolute positioning entirely**:

```css
.topbar {
    display: flex;
    justify-content: space-between;  /* left | middle | right spread out */
    align-items: center;             /* vertically center all three */
    height: 40px;
}
```

Result: `.left` hugs the left edge, `.right` hugs the right edge, `.middle` sits between them, with **no negative margins** needed.

> **Rule of thumb:** use Flexbox for layout; use `position` for special cases (overlays, badges, sticky headers).

#### 3. Making the Topbar and Sidebar Stay in Place
Like the real YouTube, we want the bars to stay visible when scrolling:

```css
.topbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 10;          /* make sure it stays above other content */
}

.sidebar {
    position: fixed;
    top: 40px;            /* start right below the 40px topbar */
    left: 0;
}
```

- **`z-index`** controls stacking order. A higher number sits on top. It only works on positioned elements.
- Fixed elements leave the flow, so the main content needs space around it: `margin-top: 40px; margin-left: 50px;`.

#### 4. Code Review: What Can We Improve?
Reading and critiquing code is a core skill. Here is our code, issue by issue.

| # | Issue | Why it matters | Fix |
|---|-------|---------------|-----|
| 1 | `.topbar` is defined in **two** CSS files with different rules | Duplicate rules are confusing and can silently override each other | Keep **one** stylesheet and merge the rules |
| 2 | `.right img { display: flex; flex-direction: row; }` | `flex-direction` only works on a flex **container** (a parent). Applying it to an `<img>` does nothing | Put `display: flex` on `.right`, not on its images |
| 3 | `.right, .imgclass { width: 15px; }` | Forces the whole right container to 15px wide, squeezing the four icons. `.imgclass` isn't used in the HTML at all | Remove it. Set `width` on `.right img` instead |
| 4 | `margin-top: -15px` and `margin-left: -7px` | Negative margins are "patches" for a deeper alignment problem | Use `align-items: center` and `justify-content` |
| 5 | `<div class="mic">` is empty | An empty box does nothing yet | Add an icon (homework from Session 2) or remove it |
| 6 | `alt=""` on every image | Fine for decorative images; bad for meaningful ones like the logo or profile photo | Write real text: `alt="YouTube logo"`, `alt="My channel"` |
| 7 | Sidebar HTML has no `<html>/<head>/<body>` and no `<link>` | A fragment can't be opened as a valid page alone | Combine with the topbar into one `index.html` |
| 8 | Very small values (`7px` text, `15px` icons) | Hard to read and click, especially on phones | Use at least ~12px text and 24px icons (our page copies a small design) |
| 9 | Long repeated lists of class names | Hard to maintain | One shared class (`.item`) |
| 10 | `body` has the browser's default **8px margin** | Creates a white gap around the page | `body { margin: 0; }` |

#### 5. A Global Reset
Browsers add default margins and sizes. A tiny reset gives predictable results:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

- `*` is the **universal selector** (every element).
- **`box-sizing: border-box`** makes `width` include the padding and border, so a `width: 100px` box is really 100px wide. This is **hugely** helpful for layouts. (Look back at the box model drawing from Session 2.)

#### 6. The Cleaned-Up Final Code

**`index.html`**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube Clone</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- TOPBAR -->
    <header class="topbar">
        <div class="left">
            <img class="hamburger-menu" src="hamburger-menu.svg" alt="Menu">
            <img class="youtube-logo" src="youtube-logo.svg" alt="YouTube logo">
        </div>

        <div class="middle">
            <input type="text" placeholder="Search">
            <button class="search-btn">
                <img src="search.svg" alt="Search">
            </button>
        </div>

        <div class="right">
            <img src="create.svg" alt="Create">
            <img src="youtube-apps.svg" alt="Apps">
            <img src="notifications.svg" alt="Notifications">
            <img class="profile" src="my-channel.jpeg" alt="My channel">
        </div>
    </header>

    <!-- SIDEBAR -->
    <nav class="sidebar">
        <div class="item">
            <img src="home.svg" alt="">
            <p>Home</p>
        </div>
        <div class="item">
            <img src="explore.svg" alt="">
            <p>Explore</p>
        </div>
        <div class="item">
            <img src="subscriptions.svg" alt="">
            <p>Subscriptions</p>
        </div>
        <div class="item">
            <img src="originals.svg" alt="">
            <p>Originals</p>
        </div>
        <div class="item">
            <img src="youtube-music.svg" alt="">
            <p>YouTube Music</p>
        </div>
    </nav>

    <!-- MAIN CONTENT (videos will go here in the next sessions) -->
    <main class="content">
        <h1>Videos coming soon...</h1>
    </main>

</body>
</html>
```

**`style.css`**
```css
/* ---------- Reset ---------- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, Helvetica, sans-serif;
}

/* ---------- Topbar ---------- */
.topbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 40px;
    padding: 0 15px;
    display: flex;
    justify-content: space-between;   /* left | middle | right */
    align-items: center;              /* vertical centering */
    background-color: white;
    border-bottom: 1px solid #ddd;
    z-index: 10;
}

.left {
    display: flex;
    align-items: center;
}

.hamburger-menu {
    width: 20px;
}

.youtube-logo {
    width: 70px;
    margin-left: 15px;
}

.middle {
    display: flex;
}

.middle input {
    width: 300px;
    padding: 6px 10px;
    font-size: 14px;
    border: 1px solid grey;
    border-radius: 3px 0 0 3px;       /* round the left side only */
}

.middle input::placeholder {
    font-size: 13px;
}

.search-btn {
    width: 40px;
    border: 1px solid grey;
    border-left: none;                /* avoid a double border */
    border-radius: 0 3px 3px 0;       /* round the right side only */
    background-color: rgb(235, 235, 235);
    cursor: pointer;
}

.search-btn img {
    width: 18px;
}

.right {
    display: flex;
    align-items: center;
    gap: 20px;                        /* even spacing, no margins needed */
}

.right img {
    width: 20px;
}

.right .profile {
    width: 28px;
    height: 28px;                     /* 1:1 ratio ... */
    border-radius: 50%;               /* ... + 50% = circle! (Session 1 homework) */
    object-fit: cover;                /* crop instead of stretching */
}

/* ---------- Sidebar ---------- */
.sidebar {
    position: fixed;
    top: 40px;                        /* sits right below the topbar */
    left: 0;
    width: 70px;
    display: flex;
    flex-direction: column;
    padding-top: 5px;
}

.item {
    display: flex;
    flex-direction: column;           /* icon above label */
    align-items: center;              /* center horizontally */
    padding: 10px 0;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.item img {
    width: 24px;
    margin-bottom: 4px;
}

.item p {
    font-size: 10px;
    text-align: center;
}

.item:hover {
    background-color: rgb(225, 224, 224);
}

/* ---------- Main content ---------- */
.content {
    margin-top: 40px;                 /* clear the fixed topbar */
    margin-left: 70px;                /* clear the fixed sidebar */
    padding: 20px;
}
```

**What changed and why:**
- One HTML file, one CSS file.
- **Semantic tags:** `<header>`, `<nav>`, `<main>` instead of anonymous `div`s. They mean something to search engines and screen readers.
- `justify-content: space-between` replaced `position: absolute` plus negative margins.
- `gap` replaced the per-image `margin: 15px`. One line gives even spacing.
- The five long class lists became one `.item` class.
- The profile picture became a circle: **1:1 ratio + `border-radius: 50%`**.
- The search button is now a real `<button>` (keyboard accessible).

#### 7. Debugging Checklist
1. **Inspect** the element in DevTools. Which rules apply? Which are crossed out (overridden)?
2. **Add a temporary outline**: `* { outline: 1px solid red; }` shows every box.
3. **Change one thing at a time** and refresh.
4. **Read the cascade:** if two rules conflict, the more specific selector wins; if equal, the one **later** in the file wins.
5. **Validate** your HTML at [validator.w3.org](https://validator.w3.org/) to catch missing closing tags.

#### 8. How CSS Decides Who Wins (Specificity Preview)

| Selector type | Strength |
|---------------|----------|
| Element (`p`) | Weakest |
| Class (`.intro`) | Medium |
| ID (`#header`) | Strong |
| Inline style (`style="..."`) | Stronger |
| `!important` | Overrides almost everything (avoid it!) |

### Resources
- [CSS `position` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [Positioning (MDN Learn)](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning)
- [CSS `z-index` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)
- [CSS `justify-content` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)
- [CSS `gap` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/gap)
- [CSS `box-sizing` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)
- [CSS `object-fit` (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
- [Cascade and Specificity (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
- [Semantic HTML (MDN)](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html)
- [Debugging CSS (MDN)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS)

### Practice Questions
1. Explain the difference between `relative`, `absolute`, `fixed` and `sticky` in your own words.
2. Why did using `position: absolute` on `.right` force us to use `margin-top: -15px`?
3. What does `box-sizing: border-box` change? Make a `200px` box with `20px` padding and `5px` border and compare both modes in DevTools.
4. Why is `<nav>` better than `<div class="nav">`?
5. Which has higher priority: an element selector or a class selector? Prove it with a small experiment.

### Homework
1. Rebuild the project using the cleaned-up code, but **change the design**: your own colors, a different logo, and different sidebar items.
2. Make the topbar and sidebar **dark mode** (dark background, light text and icons).
3. Add a **hover effect** to the topbar icons and the search button.
4. Under `<main>`, build **one video card**: a thumbnail `<img>`, a title `<p>` and a channel name `<p>`, styled with margin, padding and `border-radius`.
5. **Challenge:** repeat the video card 8 times and arrange them in a row that wraps onto the next line. (Hint: `display: flex; flex-wrap: wrap;`.)

### What's Next
With the layout done, the next step is the **video grid**, followed by **JavaScript** to make the page interactive (toggling the sidebar with the hamburger button, searching, and more).