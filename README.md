# 🚀 Jayant Shringi - Personal Portfolio

A clean, responsive, and modern personal portfolio website built with HTML5 and CSS3. Designed to showcase MERN stack developer skills, certifications, and projects.

> [!WARNING]
> **Disclaimer & Warning on Personal Details**
> Please **do not misuse** the personal details, email address, contact links, and certification credentials (such as Great Learning and Coursera links) provided in this repository. These details are unique to the project owner, **Jayant Shringi**. If you are using this project as a template or reference for your own portfolio, please ensure you replace all personal information, links, and credentials with your own.

---

## 🔗 Live Links & Socials
* **GitHub Profile**: [github.com/jayantshringi](https://github.com/jayantshringi)
* **LinkedIn Profile**: [linkedin.com/in/jayantshringi](https://linkedin.com/in/jayantshringi)
* **Email**: [jayants3125@gmail.com](mailto:jayants3125@gmail.com)

---

## 🛠️ Technologies & Features

### Core Stack
* **HTML5**: Semantic tags used to structure content for accessibility and SEO.
* **CSS3**: Modern layouts, variables, responsive design, and transitions.
* **Google Fonts**: [Inter](https://fonts.google.com/specimen/Inter) for clean text readability and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) for developers/technical branding.

### Features
* **Sticky Navigation Bar**: Stays anchored to the top of the screen on scroll.
* **Smooth Scrolling**: Implements native CSS smooth-scrolling behavior between sections.
* **Certification Section**: Styled credential cards featuring verified external links, issue dates, and status tags.
* **Interactive Hover Effects**: Subtle animations (scale/lift translate transforms) on skills tags, navigation links, and project cards.
* **Responsive Layout**: CSS Flexbox and Grid (`repeat(auto-fit, minmax(280px, 1fr))`) elements automatically reflow and scale down on tablets and mobile devices.

---

## 📁 File Structure
```text
Portfolio/
├── index.html     # Semantic HTML structure & content
├── style.css      # Core style rules, CSS variables, & responsiveness
└── README.md      # Documentation (this file)
```

---

## 🔍 Detailed Code Explanation

Below are detailed, line-by-line and section-by-section breakdowns of both the HTML and CSS files.

<details>
<summary><b>1. HTML Structure (index.html)</b></summary>

### The Document Setup
* `<!DOCTYPE html>`: Tells the web browser to render the page in standard HTML5 mode.
* `<html lang="en">`: Root tag indicating that the webpage content is in English.

### The Head Section (Metadata & Links)
* `<meta charset="UTF-8">`: Ensures all character sets (including emojis and symbols) render correctly.
* `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Critical for mobile responsiveness; sets width to follow the screen-width.
* `<title>Jayant Shringi - Portfolio</title>`: Defines the text displayed on the browser tab.
* `<link rel="stylesheet" href="style.css">`: Links the custom CSS rules sheet.

### Navigation Header
* `<header class="navbar">`: Uses semantic header tags, styled with position-sticky rules.
* `<div class="nav-container">`: Centers and spaces menu items.
* `<div class="logo">`: Monospace branding wrapper with `.highlight` class applied to "Jayant".
* `<nav>` & `<ul class="nav-links">`: Holds the lists of navigation items linking smoothly to section IDs (`#about`, `#skills`, `#projects`, `#contact`).

### Hero Section (Intro Area)
* `<section class="hero-section">`: Highlights the landing screen.
* `<h1>`: Uses a bold primary heading showing the name.
* `<p class="subtitle">`: Small subtext denoting developer status.
* `<a href="#projects" class="btn btn-outline">` & `<a href="#contact" class="btn btn-outline">`: Outlined CTA links scrolling to projects and contacts.

### About Section & Certifications
* `<section id="about">`: Contains a personal biography and credentials.
* `.certification-box`: Holds a styled list of certificates with metadata (Issued date, Status) and target-blank external links:
  * **Git Version Control** (Great Learning)
  * **Introduction to Front-End Development** (Coursera)
  * **Foundations of Cybersecurity** (Coursera)

### Skills Section
* `<section id="skills">`: Technical competencies wrapped in a flexbox layout. Includes: HTML5, CSS3, JavaScript, Git/GitHub, Data Ethics, and Security Management.

### Projects Section
* `<section id="projects">`: Dynamic grid layout containing four project cards:
  1. **Movie Cards**: Responsive CSS Flexbox layout.
  2. **College Tech Fest**: Registration website with multi-page HTML/CSS flow.
  3. **Student Quiz Portal**: Client-side examination portal built using vanilla JS.
  4. **Campus Utility Hub**: Production-grade MERN dashboard with 8 independent modules.

### Contact Section
* `<section id="contact">`: Simple card featuring buttons for quick mailto and profile links.

### Footer
* `<footer>`: Standard copyright banner.
</details>

<details>
<summary><b>2. CSS Styling (style.css)</b></summary>

### CSS Variables (The Theme)
* `:root`: Stores styling tokens like background color (`--bg-color`), main text (`--text-main`), muted text (`--text-muted`), accent blue (`--accent-color`), card background (`--card-bg`), and borders (`--border-color`). This keeps the theme clean and customizable.

### Global Reset & Defaults
* `*`: Clears browser padding, margins, and enforces `box-sizing: border-box`.
* `html`: Sets `scroll-behavior: smooth` for smooth scrolling and `scroll-padding-top: 80px` to prevent the sticky header from blocking headings.
* `body`: Sets the default Inter font family, background colors, and line-height.

### Typography
* `h2`: Styled with a custom bottom border using the pseudo-element `h2::after` to create a modern accent line.
* `.highlight`: Highlights text using the accent color.

### Layout Containers
* `.container`: Constrains main content width to 900px and centers it for optimal readability.
* `section`: Provides massive vertical spacing (`5rem`) for layout breathing room.

### Navigation Navbar
* `.navbar`: Features `position: sticky`, `top: 0`, and `z-index: 100` so it hovers on top of sections while scrolling.
* `.nav-links`: Flexbox aligns items horizontally with a `2rem` gap.

### Hero Section Layout
* `.hero-section`: Enforces vertical centering and top padding to accommodate the sticky navbar.

### Buttons & CTAs
* `.btn`: Styled after LinkedIn's pill-shaped button style (`border-radius: 24px`) with a blue transition on hover.
* `.btn-outline`: Outlined variant inspired by GitHub's secondary button design (`#f6f8fa` background and light borders).

### Cards & Grid Layouts
* `.certification-box`: Adds a top border dashed separator.
* `.cert-list li`: Uses Flexbox to space info and links across the screen width.
* `.skills-grid`: Implements `flex-wrap: wrap` to allow skill tags to wrap onto new rows dynamically.
* `.projects-grid`: Utilizes a highly robust CSS Grid rule (`grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))`) to handle column count responsively without media queries.
* `.project-card`: Standardizes white background cards, lifting on hover (`transform: translateY(-4px)`) using smooth transitions.

### Responsive Rules (Media Queries)
* `@media (max-width: 768px)`:
  * Adjusts padding and font sizes.
  * Hides standard desktop links (`.nav-links`).
  * Changes certification items to stack vertically on small screens.
</details>

---

## 💻 Local Setup & Development

To view the portfolio website on your local machine:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/jayantshringi/Portfolio.git
   ```
2. **Open index.html**:
   Open `index.html` in any web browser of your choice, or use a VS Code extension such as *Live Server* to host a local version.
