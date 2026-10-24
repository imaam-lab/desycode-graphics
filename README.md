# Desycode Graphics — Website Setup Guide

## Files
Keep all files in one folder, exactly as they are:

```
desycode-website/
├── index.html      Home
├── service.html    Services
├── price.html      Prices (from Price_List.xlsx)
├── about.html      About
├── team.html       Team (placeholders)
├── career.html     Careers + application form
├── style.css       Shared stylesheet for all pages
└── assets/
    ├── logo-wordmark.png   Full logo (used in header and footer)
    └── logo-mark.png       D icon (used in hero, about page and favicon)
```

The site uses HTML and CSS only. It contains no JavaScript. Google Fonts (Inter) and Font Awesome load from their CDNs, so the site needs an internet connection to display those.

## Preview locally
Double-click `index.html` to open it in a browser. Or run a quick local server from the folder:
`python3 -m http.server 8000`, then visit `http://localhost:8000`.

## Replace the logo
Overwrite `assets/logo-wordmark.png` and `assets/logo-mark.png` with new files of the same names. Keep the proportions, and use a transparent background for best results.

## Replace team details and portfolio placeholders
- **team.html:** replace each `[Portrait Image]`, `[Team Member Name]`, `[Job Title]`, and `[Short Biography]` with real details. To use a photo, add an `<img>` inside the `.portrait` div, for example `<img src="assets/name.jpg" alt="Name, Job Title">`.
- **index.html:** the three "Creative Concepts" cards are CSS-built placeholders. Replace each `<figure class="work">` block with a real image or project card when approved client work is available.

## Update prices
All prices are in `price.html`. Each package is a `<article class="price-card">` block. Edit the `.price` line and the feature list inside it. Keep prices in LKR and match the price list.

## Make the career form submit applications
A plain HTML form cannot deliver submissions by itself. It needs an external form service or a backend. The form in `career.html` is set up for this, and its `action` currently reads `REPLACE-WITH-FORM-ENDPOINT`. To activate it:

1. Create a form on a service such as Formspree, Getform, or Google Forms, which provides a unique endpoint URL.
2. Replace `REPLACE-WITH-FORM-ENDPOINT` in `career.html` with that URL.
3. Test by submitting a sample application.

Until this step is done, submitting the form will not deliver anything. Applicants can also reach you on WhatsApp, which is linked on the page.

## Contact details used on the site
- Phone: +94 756598911
- WhatsApp: https://wa.me/94756598911
- Instagram: https://www.instagram.com/desycode
