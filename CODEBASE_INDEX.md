# Codebase Index: Algorithmia SE GitHub Pages Website

This document serves as an index and structural overview of the **Algorithmia SE** static website, which is deployed via GitHub Pages (`ALX-SE-Algorithmia.github.io`).

## 📌 Repository Overview

This repository contains a classic **Static Website** built with vanilla web technologies (HTML, CSS, JavaScript). It serves as the primary landing page and informational hub for the Algorithmia SE consortium.

**Tech Stack:**
- **Markup:** HTML5
- **Styling:** Vanilla CSS3 (Custom stylesheets for different pages)
- **Scripting:** Vanilla JavaScript (ES6)
- **External Libraries:** 
  - FontAwesome & Unicons (Icons)
  - Google Fonts (Bentham)
  - SMTP.js & SweetAlert (Contact form submission)

---

## 📂 Directory Structure

### Root Files (HTML Pages)
* **`index.html`** 
  * **Purpose:** The main landing page.
  * **Key Sections:** Hero Section, About Us ("Our Journey"), Mission & Vision, Goals, Contact Us Form, Newsletter Subscription.
  * **Functionality:** Implements an email sending function using `smtpjs` and `sweetalert` for the contact form.

* **`projects.html`** 
  * **Purpose:** Showcase of the community's work.
  * **Key Sections:** Featured Projects, Recent Projects, Upcoming Projects.
  * **Functionality:** Includes an inline JavaScript-driven custom carousel to slide through project cards horizontally.

* **`events.html`**
  * **Purpose:** Details community events and hackathons.
  * **Key Sections:** Upcoming Events, Latest Events, Past Events.

* **`blogs.html`**
  * **Purpose:** Hub for articles, tech talks, and community writings.

* **`moved.html`**
  * **Purpose:** Acts as a redirect or informational page for moved content/links.

### Subdirectories

* **`css/`** (Styling)
  * `style.css`: The global and primary stylesheet (mainly used by `index.html`).
  * `projects.css`: Specific styling for the projects page and its card carousels.
  * `events.css`: Specific styling for the events page.
  * `blogs.css`: Specific styling for the blogs page.

* **`js/`** (Scripting)
  * `main.js`: Global JavaScript functionality.
    * Implements `IntersectionObserver` to toggle the navbar's scrolled state (transparent to solid).
    * Handles the mobile hamburger menu toggle.
    * Implements the "scroll to top" button logic.

* **`images/`** (Assets)
  * Contains all static visual assets organized contextually:
  * `home/`: Images used on the landing page (mission, vision, goals, founder).
  * `projects/`: Thumbnails for various projects (hackathons, apps, demo projects).
  * `events/`, `blogs/`, `shared/`
  * `website-logos/`: Contains SVGs and Favicons of the organization's logo.

---

## ⚙️ Key Mechanisms & Integrations

1. **Routing:**
   * No client-side router is used. Navigation works via standard `<a>` tags linking directly to `.html` files or specific section IDs (e.g., `href="./index.html#About_us"`).

2. **Contact Form:**
   * Located in `index.html`.
   * Intercepts standard form submission and uses **Elastic Email SMTP** credentials via `SMTP.js` to send messages to `algorithmiasecollaborators@gmail.com`.

3. **Responsiveness:**
   * Handled through CSS Media Queries.
   * A hamburger menu icon (`#menu-bar`) toggles the visibility of the `.nav-container` on smaller screens.

4. **Animations & Interactivity:**
   * Scroll observers add a solid background to the sticky header once the user scrolls past the hero section.
   * Project cards have a custom-built JS carousel (found inline within `projects.html`) that paginates 3 cards at a time.
