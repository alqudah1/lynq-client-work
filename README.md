# LYNQ client work

Case studies from client projects I've built through **[LYNQ](https://lynq.build)**, my web and automation studio. The client code lives in private repos, so this page explains the problem, what I built and how it works.

| Client | What they do | Live site |
|---|---|---|
| Kingsbridge Group | Custom homes and property management, GTA | [kingsbridgegroup.ca](https://www.kingsbridgegroup.ca) |
| Finding Amy | Photo booth rental, Amman | [finding-amy.com](https://finding-amy.com) |
| Arcubed Label | Handmade crochet bags, made to order | [arcubed.shop](https://arcubed.shop) |
| NASMA | Levantine restaurant, Amman | [nasmajo.com](https://nasmajo.com) |
| Kids Coding | Coding programs for kids, Toronto | [kidscoding.ca](https://kidscoding.ca) |

---

## Kingsbridge Group

**Problem:** A custom home builder and commercial property manager needed a site that explained two very different services and sent inquiries straight to the office inbox.

**What I built**
- Separate pages and inquiry forms for Custom Homes and Property Management, plus About and Contact.
- A serverless contact endpoint on Vercel that validates each inquiry and sends it to the company's Microsoft 365 mailbox through the Microsoft Graph `sendMail` API.
- The Graph app is registered in the client's Microsoft Entra tenant, and its mail access is scoped to the one company mailbox instead of every mailbox in the organization.
- A written setup guide so the client's admin can see exactly what was configured.

**Stack:** HTML, CSS, JavaScript, Vercel serverless functions, Microsoft Graph, Microsoft Entra ID

---

## Finding Amy

**Problem:** A portable photo booth business in Amman was taking every booking through Instagram DMs. Customers couldn't see open dates or prices without asking.

**What I built**
- A tap-to-start landing page with event photos.
- A **live availability calendar.** A small serverless function reads the business's Google Calendar feed and marks a day as taken only when both booth devices are booked. If the feed is down, the calendar falls back to demo data instead of breaking.
- Packages, booth-only rates, add-ons and customization options, so customers know the price before they ask.
- Booking hands off to WhatsApp with the chosen dates, because that's how the team already works.
- A digital loyalty card and a gallery of past events.

**Stack:** HTML, CSS, JavaScript, Vercel serverless functions, Google Calendar (ICS)

---

## Arcubed Label

**Problem:** A handmade bag brand sold through Instagram conversations. Every order needed back and forth about colour, size, strap and price.

**What I built**
- A made-to-order store with four bag shapes and 16 colourways, where customers choose the size, strap and chain before the bag is made.
- The Colour Atelier: customers try every colour on the same bag while its shape, texture and details stay consistent.
- Product customization, cart, checkout and order management, plus collection pages for made-to-order and ready-to-ship stock and an orders and shipping FAQ.

**Stack:** Next.js, React, TypeScript, Vercel

---

## NASMA

**Problem:** A busy Levantine restaurant with a big Instagram following had no website for its menu, hours or reservations.

**What I built**
- A bilingual (English and Arabic) site with the full menu by section, prices and a downloadable PDF.
- Reservations by phone or WhatsApp, hours, and directions.
- The restaurant's story and a food and space gallery, using its own brand colours and type.
- Mobile-first layout, since most visitors come from Instagram on a phone.

**Stack:** HTML, CSS, JavaScript, Vercel

---

## Kids Coding

**Problem:** An established kids coding school had programs, camps and classes, but parents had trouble finding the right program and registering.

**What I built**
- A rebuilt parent journey: program finder → what your child will learn → class times → registration.
- Learning chapters and session-by-session pathways for each program.
- Clearer structure for After School, Camps, Online Classes and STEM Workshops.
- Built on the client's existing Wix platform with Velo code kept in Git.

**Stack:** Wix, Velo (JavaScript), GitHub

---

### Contact
Mustafa AlQudah · [mustafaalqudah.com](https://mustafaalqudah.com) · [LinkedIn](https://www.linkedin.com/in/mustafaalqudah)
