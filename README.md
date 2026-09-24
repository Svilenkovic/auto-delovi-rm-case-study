<a href="https://autodelovirm.com/"><img src="media/cover.jpg" alt="Auto Delovi RM, home page on a laptop and a phone" width="100%"></a>

# Auto Delovi RM

Web shop for new car body parts from Zaječar, where customers pick make, model and year and pay on delivery anywhere in Serbia.

**[autodelovirm.com](https://autodelovirm.com/)** · [Case study (in Serbian)](https://svilenkovic.com/radovi/auto-delovi-rm) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Auto Delovi RM</td></tr>
  <tr><td><b>Industry</b></td><td>New body parts for passenger cars and light commercial vehicles</td></tr>
  <tr><td><b>Location</b></td><td>Zaječar, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Web shop with an admin PWA</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>Next.js 15.5, React 19, TypeScript, Tailwind 4, three.js, React Three Fiber, GSAP, Lenis, SQLite, PWA</td></tr>
</table>

## About the project

Auto Delovi RM sells new body parts, from bumpers and wings to headlights, tail lights and mirrors, and ships them by courier across Serbia with payment on delivery. Until this shop everything went through a classifieds site, where competitors shared the page and the ranking was someone else's decision. The owner wanted his own domain, a page for every part and a panel he could run from his phone.

The hardest part was not losing track of the customer's car. Make, model and year go into the URL through the History API, with no new request to the server, and the shop remembers them. Someone who shares a part on Facebook and comes back still sees parts for the same car. Search handles the way people type: filler words are dropped, a range like 04-07 becomes a year filter, and catalogue numbers match with or without spaces and dashes.

## What I built

- Parts by make, model and year, plus indexable pages for every category, make, model and their combinations
- Search with narrow synonym groups, Cyrillic input and ranking by where the word sits in the part name
- Checkout without an account: name, phone and address, cash on delivery, and a total the server recalculates from its own database
- An admin PWA for parts, vehicles, orders, inquiries, ad slots and all site text, including copying one part to several vehicles with a preview before saving
- A three.js road scene behind the home page hero that runs only on capable desktops; phones, low-end hardware and visitors who prefer reduced motion get a static image
- Title, description and canonical moved back into the `<head>` after measuring that Googlebot got them about 120,000 characters into the page

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 95 | 100 | 100 | 100 |
| Desktop | 91 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, September 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `AutoPartsStore`, `Store`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Auto Delovi RM, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Auto Delovi RM, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="The product range and an overview of all car body part groups">
<sub>The product range and an overview of all car body part groups</sub>

<img src="media/inner-2.webp" alt="Featured parts, picked by the owner in the admin panel">
<sub>Featured parts, picked by the owner in the admin panel</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
