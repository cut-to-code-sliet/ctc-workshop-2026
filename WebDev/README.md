# CTC Web Development Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: Web Basics, Terminal Commands & HTML/CSS Intro (21 Sep 2026)](#session-1-web-basics-terminal-commands--htmlcss-intro-21-sep-2026)

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