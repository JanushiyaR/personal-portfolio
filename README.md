# Janushiya Rajakumar &mdash; Portfolio

This is a simple, single-page personal portfolio site for **Janushiya Rajakumar**, an aspiring Data Engineer with a strong foundation in data science.

## 🌐 Live Portfolio

**Visit the live portfolio:** https://janushiyar.github.io/personal-portfolio/

The site is fully responsive and works seamlessly on desktop and mobile devices.

The stack is intentionally lightweight:

- **HTML5** for structure (`index.html`)
- **CSS3** for styling (`styles.css`)
- **Vanilla JavaScript** for mobile menu and form handling
- **EmailJS** for contact form submissions
- **Font Awesome 6.5** for icons
- **Google Fonts** (Poppins & Space Grotesk)

No build tools or frameworks are required.

## ✨ Features

- ✅ **Fully responsive** – optimized for mobile, tablet, and desktop
- ✅ **Mobile-friendly navigation** – hamburger menu with smooth animations
- ✅ **Working contact form** – email submissions via EmailJS
- ✅ **Smooth scroll animations** – reveal effects on page load and scroll
- ✅ **Accessible design** – semantic HTML, ARIA labels, keyboard navigation
- ✅ **Fast & lightweight** – minimal dependencies, excellent performance

## 📧 Contact Form Setup

The contact form uses **EmailJS** to send messages to your inbox:

1. Sign up at [EmailJS](https://www.emailjs.com/) (free tier available).
2. Create an email service and template with variables: `{{name}}`, `{{email}}`, `{{message}}`.
3. Get your **User ID**, **Service ID**, and **Template ID** from the dashboard.
4. Update these in `index.html` (lines ~769–784):

   ```js
   emailjs.init('YOUR_USER_ID');
   emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this);
   ```

Visitors can now send you messages directly through the portfolio.

## Running the site

You can open the portfolio directly in a browser:

1. Navigate to this folder.
2. Open `index.html` in your preferred browser.

For the best experience (especially with fonts and relative paths), you can also serve it with a simple local web server (for example, using VS Code Live Server or `python -m http.server`).

## Resume download

The **Download Resume** button in the hero section assumes a file named:

- `Janushiya_Rajakumar_Resume.pdf`

in the same folder as `index.html`.

To hook up your actual resume:

1. Copy your latest resume PDF into this folder.
2. Rename it to `Janushiya_Rajakumar_Resume.pdf`, **or**
3. Update the `href` in `index.html`:

   ```html
   <a
     class="btn btn-primary"
     href="YOUR_FILE_NAME.pdf"
     download
   >
     Download Resume
   </a>
   ```

## Color palette

The site uses your requested colors:

- Background: `#FCF6F5`
- Accent: `#2BAE66`

They are configured as CSS custom properties at the top of `styles.css`. If you want to tweak the palette, you can adjust these variables:

```css
:root {
  --bg: #fcf6f5;
  --accent: #2bae66;
  --accent-dark: #228852;
  --text-main: #111827;
  --text-muted: #6b7280;
}
```

## Customizing content

Most of the portfolio content is taken directly from your resume:

- **Hero, About, Skills, Experience, Projects, Certifications, Education, Contact**

You can edit text or add/remove sections as needed by adjusting `index.html`. Styling tweaks can be made in `styles.css`.

