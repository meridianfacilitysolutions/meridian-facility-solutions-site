MERIDIAN FACILITY SOLUTIONS - WEBSITE v2 (static HTML + CSS)
Domain: meridianfacilitysolutions.com
Status: built locally, NOT deployed. No accounts created, nothing purchased.

FILES
  index.html     Home
  services.html  Services
  about.html     About
  contact.html   Contact
  style.css      Shared stylesheet (navy #14213d, gold #c9a227, Georgia headings, Arial body)
  *.png          Screenshots (1280 wide; index-mobile.png is 390 wide)

PAGE CONTENTS
  Home: hero ("One point of accountability for your facility services"),
    "Why Meridian" value statement, 4 service cards (Janitorial & Custodial =
    launch service; Facilities Maintenance, Groundskeeping & Landscaping,
    HVAC & Building Systems = Coming soon), "How we work" 3 steps
    (Scope -> Assign crews and partners -> Quality control),
    Government registration box, call to action.
  Services: janitorial & custodial first with typical tasks, then Facilities
    Maintenance, Groundskeeping, Landscaping, HVAC & Building Systems, and
    Related Facility Services, each marked "Coming soon / planned for
    availability through our vetted partner network" with typical tasks.
  About: company story, leadership/owner bio, one-point-of-accountability
    approach, values (Accountability, Respect, Reliability, Transparency),
    service area, certifications, Government registration box.
  Contact: email (mailto link with a pre-filled inquiry template), phone,
    Fairfield CA location, website, service area, "what to include" list,
    capability statement "available on request" box, registration box.
    No form/backend.
  All pages: shared header/nav and footer, unique <title> and meta
    description, skip link, footer disclaimer that the company is private and
    not affiliated with any government agency.

PLACEHOLDERS TO FILL IN (search the files for "[Placeholder" and "PLACEHOLDER")
  1. Company story ............................. about.html
  2. Owner name and title ...................... about.html
  3. Owner bio incl. years of experience ....... about.html
  4. Service area .............................. services.html, about.html, contact.html
  5. Certifications / licenses / insurance ..... services.html, about.html (list only what you hold)
  6. Capability statement link (PDF) ........... contact.html
  7. SAM.gov registration, UEI and CAGE ........ index.html, about.html, contact.html
     (currently "[to be added after registration, expected 2027]")
  8. Additional NAICS codes as services launch . index.html
  9. Legal entity name after LLC formation ..... footer on every page
  When filled, remove the class="placeholder" / class="ph-inline" so the yellow
  dashed placeholder styling disappears.

OWNER REVIEW BEFORE BIDDING
  HTML comments on index, services and about note that on small-business
  set-aside federal service contracts FAR 52.219-14 generally requires the
  prime to perform at least 50% of the work with its own employees (work
  subcontracted to similarly situated small businesses can count). Review the
  "trained crews and vetted partners" wording so it matches how you staff
  each contract. Do not add certifications, past performance, clients,
  testimonials, or statistics you cannot document.

FREE HOSTING STEPS (not performed - do these yourself or ask for a walkthrough)
  Option A - Cloudflare Pages (free)
    1. Sign in / create a free Cloudflare account.
    2. Workers & Pages -> Create -> Pages -> "Upload assets"; name the project
       (e.g., meridian-site) and upload the contents of this folder
       (or meridian-site-v2.zip). Screenshots/README can be left out.
    3. Project -> Custom domains -> add meridianfacilitysolutions.com and
       www.meridianfacilitysolutions.com.
    4. Easiest DNS route: add the domain to Cloudflare (free plan) and, in
       Porkbun -> Domain Management -> Authoritative Nameservers, replace
       Porkbun's nameservers with the two Cloudflare gives you. Cloudflare then
       creates the records automatically. (Alternative for www only: keep
       Porkbun DNS and add a CNAME "www" -> <project>.pages.dev.)
  Option B - GitHub Pages (free)
    1. Create a public repo, upload these files to the root, then
       Settings -> Pages -> Deploy from branch (main, /root).
    2. Settings -> Pages -> Custom domain: meridianfacilitysolutions.com;
       tick "Enforce HTTPS" once available.
    3. In Porkbun DNS: add A records for the apex (@) to 185.199.108.153,
       185.199.109.153, 185.199.110.153, 185.199.111.153, and a CNAME
       "www" -> <github-username>.github.io. Delete Porkbun's default
       parking/ALIAS records for @ and www first.
  DNS changes can take from minutes up to 24-48 hours to take effect.
  Note: if you set up email on the domain later, keep any MX records intact.
