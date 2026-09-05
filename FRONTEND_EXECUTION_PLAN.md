# Meem Academia Frontend Restoration & Expansion Plan

**Status:** Research and planning only — implementation will begin only after approval (“Go”).  
**Prepared:** 5 September 2026

## 1. Executive objective

Create a presentation-ready, production-quality frontend that faithfully restores every meaningful piece of public information available on the existing Meem Academia/Tarbiyah Online website, while improving its information architecture, accessibility, navigation, responsiveness, and conversion flow.

The result should feel like the website Meem Academia is *supposed* to have: spiritually grounded, academically credible, operationally clear, and easy for students, parents, instructors, sponsors, and partners to use.

## 2. Research completed

### Sources inspected

- Every discoverable public route on `courses.meemacademy.org`
- Public homepage, About, Courses, Faculty, Instructor, Blog, Contact, and legal content
- Authentication and OTP screens
- All linked JavaScript route and API definitions
- Public Meem administration APIs for courses, blogs, teachers, banners, and currencies
- Course API pagination, including records not visible in the first course-page response
- Footer, social, telephone, email, map, enrollment, sponsorship, and account links
- Original image assets for courses, faculty, blogs, mission, vision, instructor, and sponsorship content

### Important research findings

1. The original site has **no working public sitemap.xml or robots.txt**.
2. The Courses screen uses paginated/infinite API loading. It contains **18 courses**, not nine.
3. Four currencies are supported by the original API: PKR, USD, GBP, and AED.
4. The original public faculty API contains richer data than the faculty cards show, including experience, languages, roles, biographies, and images.
5. The original blog API contains six published records. Five are meaningful articles; one appears to be accidental test content.
6. Several original footer items are dead links or point back to the homepage: FAQs, Learning Resources, Jobs, LinkedIn, and Twitter.
7. Several labels and descriptions are inconsistent or mistakenly reused (for example, STEM copy on Islamiat and Urdu cards).
8. Branding alternates between Meem Academia, Meem Academy, Meem School, and Tarbiyah Online.
9. The public flow also contains account and transaction-related screens: login, registration, forgot password, OTP verification, checkout, enrollment, wishlist, invoices, bank payment, promo code, and meetings.
10. The strongest and most consistent organizational idea is **Tarbiyah**: knowledge should transform character, reconnect learners with Divine guidance, build relevant skills, and produce beneficial influence in families and society.

## 3. Organizational understanding to guide the redesign

### Core purpose

Meem Academia is not simply a course marketplace. It presents itself as a holistic learning organization that combines:

- Divine guidance and Quranic understanding
- Prophetic character and Seerah
- Arabic language
- Tarbiyah and life skills
- School-subject support
- STEM and professional skills
- Coaching, counseling, and mentorship

### Intended audiences

- Children and young learners
- Teenagers and university-age learners
- Parents and families
- Working professionals
- Arabic and Quran students
- School students needing subject support
- Prospective instructors
- Sponsors and donors
- Coaching and counseling clients

### Proposed positioning

> A modern, globally accessible learning ecosystem that turns knowledge into character, capability, and beneficial action.

### Brand architecture to clarify

- **Meem Academia** — master digital learning brand
- **Tarbiyah Online** — philosophy and/or Islamic development pathway
- **Meem School** — related school/campus identity, explained rather than mixed invisibly

A dedicated “Our Ecosystem” section/page should explain this relationship clearly.

## 4. Current frontend coverage

The current recreation includes:

- Homepage
- About
- Course catalogue
- 18 course cards and detail routes
- Faculty listing
- Instructor application
- Blog listing and six article routes
- Contact
- FAQ
- Resources
- Jobs
- Login, registration, and password reset
- Terms, privacy, and deletion pages
- Human-readable site directory
- XML sitemap and robots.txt
- Responsive navigation, search, filters, forms, and mobile layouts

This is a strong foundation, but it is not yet the final “nothing is missing” frontend.

## 5. Remaining frontend gaps

### A. Content fidelity gaps

- Several course detail pages currently summarize long original descriptions instead of preserving every topic, objective, session count, recommended book, and case-study detail.
- Blog articles need to use the exact meaningful original text rather than editorial summaries.
- Faculty needs exact experience, fluent languages, biography, teaching role, and original profile imagery where available.
- Coaching services from the homepage need full pages and booking flows:
  - Spiritual Coaching — Maulana Adnan Borana
  - Business & Life Coaching — Janzaib Borana
  - Professional Academic Counseling — Sir Rizwan
- Mission, vision, philosophy, craft, and influence content should be expanded into structured detail pages rather than only homepage blocks.
- Contact information needs one authoritative, consistent set of official numbers and email addresses, while department-specific numbers remain clearly labeled.
- Legal text should retain the full meaning of the source while correcting legacy “Source Code Academia” references only where approved.

### B. Information architecture gaps

The following useful pages should be added even where the original site has only dead labels or non-clickable text:

1. Our Philosophy
2. Our Teaching Method / The Craft
3. Our Impact / The Influence
4. Our Ecosystem (Meem Academia, Tarbiyah Online, Meem School)
5. Islamic Studies pathway
6. Quran pathway
7. Arabic pathway
8. STEM pathway
9. School Subjects pathway
10. Life Skills and Character pathway
11. Coaching hub
12. Three individual coaching-service pages
13. Faculty profile pages
14. Sponsor a Student page
15. Admissions process
16. Fees and group plans
17. Technology and online-class guide
18. Parent guide
19. Student guide
20. Instructor guide
21. Blog topic/tag pages
22. Individual learning-resource pages
23. Individual job-detail pages
24. Accessibility statement
25. Complete site directory

### C. Interaction gaps

All visible interactive cues should have a destination or behavior:

- Every course card, pathway, faculty card, service card, statistic CTA, article, resource, and job card
- Search with visible result count and no-results guidance
- Course filters aligned to the actual data model
- Faculty search and subject/language filters
- Blog search and topic filters
- Currency selector for PKR, USD, GBP, and AED
- Share actions for blog articles and course pages
- Copy-link actions
- Working accordion states
- Newsletter success/error states
- Form validation and accessible error messages
- Enrollment status labels and waitlist behavior
- Booking calendars represented as frontend flows
- Sponsor amount and course selection frontend flow
- Saved/wishlist state represented locally until backend integration
- Mobile menu, keyboard navigation, focus states, and skip-to-content

### D. Missing frontend states

Every data-driven area needs designed states for:

- Loading
- Empty results
- No schedule announced
- Enrollment closed
- Waitlist available
- Error loading content
- Offline/network error
- Form submitting
- Form success
- Form validation error
- Invalid course/blog/faculty ID
- 404 page

### E. Quality and trust gaps

- Consistent naming and capitalization
- Corrected spacing and grammar
- Honest distinction between verified source facts and proposed marketing copy
- Removal/quarantine of visible test data such as “Nimra tester” and the test blog, without silently changing underlying course facts
- Consistent phone and mail links
- Real social destinations or clearly omitted unavailable platforms
- SEO titles and descriptions per route
- Open Graph image and metadata per course/article
- Structured data for Organization, Course, Article, FAQ, Person, and BreadcrumbList
- Image alt text and semantic headings
- WCAG-oriented contrast and keyboard support

## 6. Target frontend sitemap

### Primary

- `/`
- `/about-us`
- `/our-ecosystem`
- `/contact-us`
- `/site-map`

### Philosophy and impact

- `/philosophy`
- `/teaching-method`
- `/impact`
- `/mission-and-vision`

### Courses and pathways

- `/courses`
- `/pathways/islamic-studies`
- `/pathways/quran`
- `/pathways/arabic-language`
- `/pathways/stem`
- `/pathways/school-subjects`
- `/pathways/life-skills`
- `/course-details/:id` for all 18 source courses

### Faculty and coaching

- `/faculty`
- `/faculty/:id` for every approved public instructor
- `/coaching`
- `/coaching/spiritual`
- `/coaching/business-and-life`
- `/coaching/academic-counseling`
- `/coaching/book`
- `/become-instructor`

### Admissions and support

- `/admissions`
- `/fees-and-plans`
- `/sponsor-a-student`
- `/parent-guide`
- `/student-guide`
- `/online-learning-guide`
- `/faq`

### Insights and resources

- `/blog`
- `/blog-details/:id` for valid published articles
- `/insights/:topic`
- `/resources`
- `/resources/:slug`

### Careers

- `/jobs`
- `/jobs/:slug`

### Account-flow frontend

- `/login`
- `/sign-up`
- `/forget-password`
- `/otp-verification`
- `/checkout-payment`
- `/enrollment-confirmation`
- `/payment-status`

### Legal and standards

- `/terms`
- `/privacy-policy`
- `/data-deletion`
- `/accessibility`

The final XML sitemap will include all indexable public routes and exclude private/authentication transaction screens where appropriate.

## 7. Implementation plan

### Phase 1 — Source-of-truth content model

1. Export all 18 course records from the public API.
2. Normalize titles, categories, durations, sessions, schedules, languages, levels, prices, and enrollment states without losing source information.
3. Preserve exact long descriptions, learning objectives, module lists, requirements, case-study methods, and recommended books.
4. Export all approved faculty records and separate public professional details from private data such as personal email addresses and phone numbers.
5. Import exact meaningful blog text and mark the test article as excluded from public presentation.
6. Create a central content schema instead of keeping all data inside one React file.
7. Add editorial notes identifying source inconsistencies for owner review.

**Deliverable:** structured `data/` modules for courses, faculty, articles, services, pathways, FAQs, jobs, resources, and organization details.

### Phase 2 — Architecture and reusable components

1. Introduce a real routing layer.
2. Split the monolithic React file into pages, layouts, components, and data modules.
3. Build reusable page heroes, cards, filters, breadcrumbs, CTAs, forms, schedules, pricing plans, metadata, and empty/error states.
4. Add a consistent header mega-menu and complete footer.
5. Add breadcrumbs throughout the site.
6. Implement per-page metadata and structured data.

**Deliverable:** maintainable frontend architecture suitable for later backend integration.

### Phase 3 — Complete public content pages

1. Rebuild Home around Meem’s real philosophy, audiences, pathways, featured courses, faculty, coaching, impact, sponsorship, and articles.
2. Expand About into mission, vision, philosophy, method, influence, and ecosystem pages.
3. Build six pathway landing pages connected to their relevant courses.
4. Build all 18 full course pages using source data.
5. Build a complete faculty directory and individual faculty profiles.
6. Build the coaching hub and service pages.
7. Build the full blog and topic pages.
8. Build admissions, fees, sponsorship, guides, FAQs, resources, jobs, contact, and legal pages.

**Deliverable:** every meaningful item has a destination; no fake `#` links.

### Phase 4 — Complete frontend flows

1. Course discovery: search, category filters, level, age, duration, language, enrollment state, sort, and result count.
2. Course conversion: detail → schedule → plan → account/checkout preview.
3. Instructor discovery: search, expertise, language, and profile pages.
4. Coaching: service comparison → coach/service page → booking form → confirmation.
5. Sponsorship: select course/amount → sponsor details → confirmation preview.
6. Careers: job list → job detail → application.
7. Account: login → forgot password → OTP → reset; registration → OTP → confirmation.
8. Contact and newsletter with complete validation and success states.
9. Local wishlist/saved-course behavior pending backend connection.
10. Currency display for the four currencies supported by the source API.

**Deliverable:** a fully navigable and demonstrable frontend where every flow can be shown to the owner.

### Phase 5 — Quality, accessibility, and performance

1. Responsive testing at mobile, tablet, laptop, and large desktop widths.
2. Keyboard and screen-reader checks.
3. Heading hierarchy, labels, error messaging, alt text, and focus styles.
4. Optimize/compress all original images without replacing them with unrelated stock media.
5. Lazy-load non-critical images and split page bundles.
6. Validate every internal route and external contact/social link.
7. Create redirect aliases for original misspellings such as `/faculity`.
8. Confirm direct loading of every SPA route on Cloudflare.
9. Generate sitemap.xml, robots.txt, canonical links, and route-level metadata.
10. Run a final frontend content-parity checklist.

**Deliverable:** polished, fast, accessible, presentation-ready website.

## 8. Content policy during restoration

- Original Meem images remain the visual source of truth.
- Source facts are preserved.
- Obvious typographical mistakes are corrected.
- Test data is not presented as real institutional content.
- Missing explanatory copy can be reconstructed from Meem’s stated philosophy, but it will be marked internally as proposed copy.
- Private faculty data exposed by an API will not be placed on public pages.
- Claims such as student counts, success rates, accreditation, and global reach will be retained only if they already appear publicly or are approved by the owner.

## 9. Definition of frontend completion

The frontend will be considered complete when:

- All 18 courses appear and have full detail pages.
- All approved faculty records appear and have profile pages.
- All meaningful original blog content is preserved.
- Every navigation label, card, CTA, footer item, and apparent interaction has a valid destination or behavior.
- There are no placeholder `#` links.
- There are no unexplained dead ends.
- All proposed new pages are connected through navigation and breadcrumbs.
- Every form has validation, loading, success, and error states.
- Every route works when loaded directly on Cloudflare.
- Mobile, tablet, and desktop layouts are complete.
- The final route/link audit reports zero broken internal links.
- The sitemap accurately reflects all public routes.
- Backend-dependent behavior is clearly represented without pretending transactions have occurred.

## 10. Proposed execution sequence after “Go”

1. Refactor architecture and centralize content data.
2. Complete exact course and faculty data restoration.
3. Build the expanded sitemap and navigation system.
4. Implement public information pages.
5. Implement faculty, coaching, admissions, sponsorship, resources, and careers.
6. Implement frontend-only account, enrollment, payment, and OTP flows.
7. Add metadata, structured data, accessibility, and responsive refinements.
8. Run automated route/link checks and production build.
9. Push one reviewed release to GitHub.
10. Verify the Cloudflare deployment route by route.

## 11. Items that will require owner confirmation later

These do not block frontend implementation, but should be verified before a final production launch:

- Official master brand name and relationship between Meem Academia, Meem Academy, Meem School, and Tarbiyah Online
- Authoritative general, admissions, accounts, and WhatsApp numbers
- Correct official email address
- Whether “Nimra tester” is a real category or test data
- Whether the test blog should be removed
- Accreditation claims for STEM courses
- Accuracy of “500+ sponsored students” and “95% success rate”
- Current course enrollment availability and batch dates
- Coaching biographies, availability, and fees
- Approved public faculty biographies
- Refund and registration-fee wording
- Active LinkedIn and X/Twitter profiles

---

**Approval gate:** No implementation described above will begin until the user explicitly says **Go**.
