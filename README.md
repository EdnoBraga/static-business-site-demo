# Demo Co. — static business site

Four pages, hand-written HTML5 and CSS3. No framework, no build step, no JavaScript.
Upload the folder as it is; nothing needs configuring to make it run.

```
index.html  about.html  services.html  contact.html
css/style.css
img/placeholder.svg
robots.txt  sitemap.xml  schema-template.json
```

## Applying your brand

Open `css/style.css`. The first block sets every colour and font used on the site:

```css
--brand         main colour: header links, buttons, numbers, footer
--brand-dark    darker shade: button hover, footer background
--accent        highlight: rules under headings, logo notch, link underlines
--font-heading  headings
--font-body     body text
```

Change them there and the whole site follows. One caveat worth stating plainly:
if your heading font is not already on the visitor's computer, changing
`--font-heading` is not enough — the font file has to be loaded first, with an
`@font-face` rule or a link to your font provider. Send the files or the font
name and this is set up for you.

## Your images

`img/placeholder.svg` marks each image slot. Replace it with your photographs,
keeping the `width` and `height` attributes on the `<img>` tag so the page does
not jump while images load.

## Before going live

- Remove `<meta name="robots" content="noindex, nofollow">` from the four pages.
- Add `<link rel="canonical" href="https://yourdomain.com/…">` to each page.
- Replace `YOURDOMAIN.com` in `robots.txt` and `sitemap.xml`.
- Fill in `schema-template.json` and paste it into the `<head>` as
  `<script type="application/ld+json">`. It is left as a separate file on
  purpose: publishing structured data with placeholder details would tell
  Google a company name, phone number and address that do not exist.
- Point the contact form at your hosting's form handler.

## Tested on

Chrome, Firefox, Safari and Edge, from 320px to 1440px wide.
Text contrast meets WCAG 2.2 AA throughout; the site is operable by keyboard.
