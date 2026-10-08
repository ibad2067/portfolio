# AGENTS.md — Portfolio Project Context

## Project Owner
- **Name:** Ebad-ur-Rehman Rajput
- **Email:** ebadurrehman881@gmail.com
- **Phone:** (+92) 332 204 6126
- **Location:** Nawabshah, Sindh, Pakistan
- **Role Target:** Infrastructure & Network Engineer (NOT a student — graduated August 2026)
- **Education:** BS Computer Science, QUEST Nawabshah (2022–2026)

---

## Live URLs
- **GitHub Pages (primary):** https://ibad2067.github.io/portfolio/
- **GitHub Repo:** https://github.com/ibad2067/portfolio
- **Vercel alias (legacy, may not render):** https://portfolio-smoky-seven-23.vercel.app

---

## Technical Structure
- **Single-file architecture:** `index.html` (~1970 lines) — all HTML, CSS (inline `<style>`), and JS (inline `<script>`) in one file
- **Fonts:** Space Grotesk (headings/body) + Space Mono (monospace/labels) via Google Fonts CDN
- **Images:** `images/` directory with profile photo, company logos, project screenshots, and certificates
  - `profile.jpg` — Hero photo (arms crossed, green circle background, 800x800, source `Screenshot (245).png` white-card crop)
  - `dwp-logo.png`, `habib-logo.jpg`, `biut-logo.svg` — company logos
  - `ips-ids-system.png`, `multi-site-1.png`, `multi-site-2.png`, `multi-site-topology.png` — project assets
  - `certificates/os-security.jpg`, `certificates/network-cloud.jpg`, `certificates/mern-stack.jpg` — certification images
- **No build step:** Pure static HTML/CSS/JS, no frameworks, no bundler
- **Deployment:** GitHub Pages serves `index.html` from repo root

---

## Design Tokens (Warm Beige Theme, blue accents kept)
```css
:root {
  --bg:       #f3eee3;     /* main background - warm beige */
  --surface:  #fbf9f4;     /* card/section bg - off-white */
  --surface2: #f7f3ea;     /* input bg */
  --panel:    #ece5d6;     /* tag bg */
  --accent:   #2563eb;     /* primary blue (unchanged) */
  --accent2:  #4f46e5;     /* secondary indigo */
  --accent3:  #059669;     /* green accent */
  --green:    #059669;     /* same as accent3 */
  --text:     #26221a;     /* main text - warm near-black */
  --muted:    #6f6757;     /* secondary text - warm gray */
  --faint:    rgba(37,99,235,0.07);   /* hover bg */
  --border:   rgba(60,48,25,0.14);    /* warm borders */
  --glow:     rgba(37,99,235,0.16);   /* glow effects */
  --radius:   6px;
  --nav-h:    64px;
}
```
- Hardcoded warm derivatives: nav `rgba(251,249,244,0.88)`, drawer `rgba(251,249,244,0.98)`, zoom-hint `rgba(255,253,248,0.96)`, system-tag `rgba(255,253,248,0.78)`, photo-frame gradient `#f5efe4 → #e2d8c6`, grid overlay `rgba(90,70,35,0.05)`, hover/entrance shadows `rgba(70,55,25,*)`, orbs `rgba(37,99,235,0.13)`/`rgba(99,102,241,0.12)` (blue glows kept deliberately)
- Kept intentionally dark: lightbox `rgba(24,27,33,0.96)`, modal scrim `rgba(0,0,0,0.7)`; red `#ef4444` unchanged; watermark stroke stays `rgba(37,99,235,0.22)`
- `btn-primary`/`nav-hire` use `color:var(--bg)` on accent bg — beige text on blue, contrast fine

---

## Sections (in order)
1. **Nav** — Fixed top bar with "ER." logo, nav links (About, Skills, Projects, Experience, Certs, Awards, Education, Contact), blue "Hire Me" pill, mobile hamburger
2. **Hero** — Centered layout: circular 3D photo (`#photoCard`, white ring + glow) with "Open to Opportunities 2026" caption chip below, `// System Profile` tag, "Hello, I'm Ebad-ur-Rehman Rajput", bio, 3 skill chips, View My Work / Contact Me CTAs, animated glow orbs (`.hero-orb-a/b`)
3. **About** (01) — Bio, info cards row (`auto-fit minmax(150px)`), circuit board SVG visual
4. **Skills** (02) — 6 skill cards: Networking, Infrastructure, Cybersecurity, Databases, Programming, Office & Soft Skills
5. **Projects** (03) — 5 project cards + "+ Add Project" button with modal
6. **Experience** (04) — Alternating center timeline (desktop ≥769px: odd items right-aligned left of line, even items right of line; mobile: left line), date chips, 3 internships newest-first: BIUT → DWP → Habib
7. **Certifications** (05) — 3 verified cert cards (image + lightbox, issuer badge, date, Verify link, skills tags) + "+ Add Certification" dashed slot → modal (localStorage `customCerts`)
8. **Achievements** (06) — 3 achievement cards
9. **Education** (07) — 2 education cards (BS CS + HSSC)
10. **Contact** (08) — Email, phone, location links
11. **Footer** — Copyright line

Every section header uses a **large outlined watermark number** (`.section-num`: absolutely positioned, `-webkit-text-stroke:1.5px rgba(37,99,235,0.22)`, `color:transparent`, behind the title; contact's is centered via `.contact-wrapper .section-num`).

---

## Certifications (real, verified)
1. **Introduction to Computers and Operating Systems and Security** — Microsoft via Coursera, Issued Oct 4, 2026
   - Verify: https://coursera.org/verify/T7FZY0PRQ9QW
   - Image: `images/certificates/os-security.jpg`
2. **Introduction to Networking and Cloud Computing** — Microsoft via Coursera, Issued Oct 7, 2026
   - Verify: https://coursera.org/verify/70ZDW0AB5IY
   - Image: `images/certificates/network-cloud.jpg`
3. **MERN Stack Development** — Sukkur IBA University / IS&T Dept, Govt of Sindh (IT Industry Readiness Bootcamp at QUEST Nawabshah)
   - Verify: https://verifybootcamp.netlify.app/certificate/4540294379791
   - Image: `images/certificates/mern-stack.jpg`

---

## Internship Details
1. **DWP Technologies** — ICT Network Engineer, July 2025 — August 2025, Karachi (Internship)
   - Configured/monitored enterprise routers and switches
   - Network troubleshooting (IP config, DNS resolution)
   - Security awareness training, firewall policy review
   - Data protection and access control systems
   - Logo: `images/dwp-logo.png`

2. **BIUT** — System Specialist (Intern), June 2026 — July 2026, Nawabshah
   - Technical support for hardware/software/network
   - OS installation, configuration, maintenance
   - User accounts, access permissions, backups
   - Infrastructure reliability and documentation
   - Logo: `images/biut-logo.svg`

3. **Habib Sugar Mills Limited** — Network Engineer, June–July 2024, Nawabshah (Internship)
   - Admin-side operations and industry network infrastructure
   - Network support across production and distillery divisions
   - Enterprise-level network administration
   - Logo: `images/habib-logo.jpg`

---

## Project Details
1. **ZEROSHIELD** — Final Year Thesis
   - AI framework for behavior-based zero-day attack detection
   - Enterprise network security monitoring, automated incident response
   - Anomaly detection for previously unseen attack vectors

2. **Sentinel IDS** — AI/Security
   - AI-powered intrusion detection system
   - RandomForest model on NSL-KDD dataset, 77.6% accuracy
   - Real-time packet scanning, threat classification, automated alerts
   - Dashboard with threat heatmap, live event feed, explainable AI
   - **Live:** https://sentinel-ids.onrender.com/dashboard

3. **HealBook** — Healthcare
   - Healthcare platform connecting patients with doctors/dietitians
   - Full-stack, real-time appointment booking, secure payments
   - Practitioner verification, responsive UI, search/filter
   - **Live:** https://healbook-nine.vercel.app/

4. **IPS & IDS System** — Security
   - Host-based intrusion prevention and detection system
   - Rule-based detection engine for malicious patterns
   - Real-time alerting with automated response (block IP, terminate process)
   - Tested against port scans, brute force, malware signatures

5. **Multi-Network Enterprise** — Networking (Cisco Packet Tracer)
   - Multi-site enterprise network topology
   - VLAN segmentation (Finance, HR, IT) with inter-VLAN routing
   - DHCP pools, DNS servers, email services across subnets
   - Extended ACLs for department-specific access policies

---

## Achievements
1. **Ignite AI Wrapper Competition 2026** — 3rd Position, Sindh Region
2. **International Conference Participant** — Computing Science & Technology
3. **HSSC A1 Grade** — 96% score

---

## Interactive Features
- **Add Project Modal:** "+ Add Project" button opens a form (name, badge, description, bullets, live/GitHub URLs), saves to localStorage, renders dynamic cards with delete buttons
- **Add Certification Modal:** "+ Add Certification" slot/button opens form (name, issuer, skills, image upload). Image compressed via canvas → dataURL → localStorage `customCerts`. Esc closes modal.
- **Cert Lightbox:** Clicking a cert image opens full-size view with caption; Esc closes.
- **Hero Cursor Parallax:** Desktop (`pointer:fine`) — mousemove over `#hero` drives photo 3D tilt (±16°/±14°), name translate (±18px), chips counter-drift (±8px); resets on mouseleave. Entry `fadeUp ... forwards` animations are cleared via `animationend` (sets `animation:none; opacity:1`) so JS transforms are not blocked by fill-mode.
- **Always-on Photo Float:** `.photo-frame` runs `photoFloat` keyframes (±5° rotateY, ±10px bob, 7s loop, delay 1.4s) — visible 3D motion on ALL devices, independent of mouse; `perspective:1000px` on `.photo-card`. JS tilt (card) and float (frame) are separate elements so they never conflict.
- **Scroll Reveal:** IntersectionObserver adds `.visible` class to `.reveal` elements for fade-in on scroll (`.reveal` starts visible as fallback — opacity:0 removed to fix blank page bug)
- **Nav Active Link:** Highlights current section on scroll
- **Skill Card Tilt:** 3D tilt effect on hover (desktop only, pointer:fine) — applies to `.skill-card, .project-card, .achievement-card, .cert-card, .edu-card`
- **Mobile Nav:** Hamburger toggle with slide-down drawer

---

## CSS Architecture Notes
- All CSS is inline in `<style>` tag (no external stylesheets)
- Sections alternate between `var(--bg)` and `var(--surface)` backgrounds with border separators
- `.reveal` class: scroll animation — starts `opacity:0; translateY(32px) scale(0.97)`, IntersectionObserver adds `.visible` → `scale(1)` (scale added for punchier entry motion)
- Hero: centered stack with circular photo (border-radius:50%, white ring, soft shadow), cursor parallax, glow orbs, skill chips (animations restored after `</style>` fix)
- Cards use `var(--radius)` (6px), `var(--border)`, and warm-tinted hover shadows `rgba(70,55,25,0.10)` + accent glow
- `body::before` (SVG noise texture) and `body::after` (grid pattern) pseudo-elements exist and work now that `</style>` is closed
- Responsive breakpoints: 1024px (hide hero stats), 960px (photo width/chips), 800px (single-column about), 769px (alternating timeline desktop), 768px (mobile nav), 520px (compact layout, full-width buttons), 480px (contact stack)

---

## Deployment History & Known Issues
### Root Cause
The `<style>` tag was never closed (`</style>` was missing). The browser treated all HTML content as CSS text, resulting in a blank page on ALL deployment platforms (Vercel and GitHub Pages alike). This was present since early in development.

### Fix
Added `</style>` before `</head>`. Restored hero animations, scroll reveal, and decorative pseudo-elements.

### Vercel (abandoned)
- Project renamed from `portfolio` to `ebad-portfolio`
- Deployed via `vercel --yes --prod` from CLI
- Persistent blank page issue despite multiple fixes:
  - Removed `body::before` z-index:1000 → z-index:-1
  - Removed `body::after` z-index:0 → z-index:-1
  - Moved modal HTML before `<script>` tag
  - Removed ALL `opacity:0` from hero elements
  - Removed `.reveal` opacity:0
  - Removed `prefers-reduced-motion` media query
  - Removed both `body::before` and `body::after` pseudo-elements entirely
- **Root cause was likely Vercel caching/build issue**, not code

### GitHub Pages (current)
- Repo: `ibad2067/portfolio` (public)
- Pages enabled on `master` branch, root `/`
- URL: https://ibad2067.github.io/portfolio/

---

## Deployment Commands
```powershell
# Set PATH for gh CLI (needed in new PowerShell sessions)
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")

# Commit and push changes
git add -A
git commit -m "Description of changes"
git push origin master
```

---

## File Structure
```
C:\Users\Mehbob\Downloads\ebad-portfolio\   (clone of ibad2067/portfolio)
  index.html          — Main portfolio file (all HTML/CSS/JS, ~1970 lines)
  AGENTS.md           — This context file
  .gitignore          — Ignores OS files, IDE files, .env, node_modules, .vercel
  images/
    profile.jpg       — Hero profile photo (arms crossed, 800x800)
    dwp-logo.png      — DWP Technologies logo
    habib-logo.jpg    — Habib Sugar Mills logo
    biut-logo.svg     — BIUT logo
    ips-ids-system.png
    multi-site-1.png
    multi-site-2.png
    multi-site-topology.png
    certificates/
      os-security.jpg     — Microsoft/Coursera OS & Security cert
      network-cloud.jpg   — Microsoft/Coursera Networking & Cloud cert
      mern-stack.jpg      — Sukkur IBA MERN Stack cert
```

---

## Source Assets (on disk, not in repo)
- Cert/profile screenshots: `C:\Users\Mehbob\OneDrive\Pictures\Screenshots 1\`
  - `Screenshot (245).png` — current profile photo source (1920x1080 dark canvas, white 429x429 card centered at x=744..1172/y=324..752; cropped + upscaled to 800x800 → `images/profile.jpg`)
  - Cert screenshots 243/244/246 → certificates (verified correct via Windows OCR: network-cloud/os-security/mern-stack)
  - `Screenshot (244).png` → OS & Security cert
  - `Screenshot (243).png` → Networking & Cloud cert
  - `Screenshot (246).png` → MERN Stack cert
- Old portfolio history: restored via `git clone https://github.com/ibad2067/portfolio.git`
- Design reference: 3D portfolio (Sushmita Dasari style) — dark ambient glow, photo card, skill chips, Hire Me pill
- Note: A separate Vite/React/Three.js project exists at `Downloads\portfolio` — NOT in use; user chose the old HTML portfolio
