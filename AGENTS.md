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
- **Single-file architecture:** `index.html` (~1870 lines) — all HTML, CSS (inline `<style>`), and JS (inline `<script>`) in one file
- **Fonts:** Space Grotesk (headings/body) + Space Mono (monospace/labels) via Google Fonts CDN
- **Images:** `images/` directory with profile photo, company logos, project screenshots, and certificates
  - `profile.jpg` — Hero photo (arms crossed, green gradient circle)
  - `dwp-logo.png`, `habib-logo.jpg`, `biut-logo.svg` — company logos
  - `ips-ids-system.png`, `multi-site-1.png`, `multi-site-2.png`, `multi-site-topology.png` — project assets
  - `certificates/os-security.jpg`, `certificates/network-cloud.jpg`, `certificates/mern-stack.jpg` — certification images
- **No build step:** Pure static HTML/CSS/JS, no frameworks, no bundler
- **Deployment:** GitHub Pages serves `index.html` from repo root

---

## Design Tokens (Dark Theme)
```css
:root {
  --bg:       #0f1419;     /* main background - dark navy */
  --surface:  #1a2030;     /* card/section bg */
  --surface2: #1e2738;     /* input bg */
  --panel:    #252f3f;     /* tag bg */
  --accent:   #60a5fa;     /* primary blue */
  --accent2:  #818cf8;     /* secondary indigo */
  --accent3:  #34d399;     /* green accent */
  --green:    #34d399;     /* same as accent3 */
  --text:     #e2e8f0;     /* main text - light gray */
  --muted:    #8892a4;     /* secondary text */
  --faint:    rgba(96,165,250,0.08);  /* hover bg */
  --border:   rgba(96,165,250,0.15);  /* borders */
  --glow:     rgba(96,165,250,0.2);   /* glow effects */
  --radius:   4px;
  --nav-h:    64px;
}
```

---

## Sections (in order)
1. **Nav** — Fixed top bar with "ER." logo, nav links (About, Skills, Experience, Projects, Certs, Awards, Education, Contact), green "Hire Me" pill, mobile hamburger
2. **Hero** — 3D photo card (mouse tilt, `#photoCard`) + `// System Profile` tag, "Hello, I'm Ebad-ur-Rehman Rajput", bio, 3 skill chips (with hover tilt), View My Work / Contact Me CTAs, animated glow orbs (`.hero-orb-a/b`)
3. **About** (01) — Bio, contact info grid, circuit board SVG visual
4. **Skills** (02) — 6 skill cards: Networking, Infrastructure, Cybersecurity, Databases, Programming, Office & Soft Skills
5. **Experience** (03) — Timeline with 3 internships
6. **Projects** (04) — 5 project cards + "+ Add Project" button with modal
7. **Certifications** (05) — 3 verified cert cards (image + lightbox, issuer badge, date, Verify link, skills tags) + "+ Add Certification" dashed slot → modal (localStorage `customCerts`)
8. **Achievements** (06) — 3 achievement cards
9. **Education** (07) — 2 education cards (BS CS + HSSC)
10. **Contact** (08) — Email, phone, location links
11. **Footer** — Copyright line

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
1. **DWP Technologies** — ICT Network Engineer, March 2026, Karachi (Internship)
   - Configured/monitored enterprise routers and switches
   - Network troubleshooting (IP config, DNS resolution)
   - Security awareness training, firewall policy review
   - Data protection and access control systems
   - Logo: `images/dwp-logo.png`

2. **BIUT** — System Specialist (Intern), June–Aug 2025, Nawabshah
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
- **Hero Photo Tilt:** Mouse-move 3D tilt on `#photoCard` (perspective on `.photo-col`); skill chips have hover tilt.
- **Scroll Reveal:** IntersectionObserver adds `.visible` class to `.reveal` elements for fade-in on scroll (`.reveal` starts visible as fallback — opacity:0 removed to fix blank page bug)
- **Nav Active Link:** Highlights current section on scroll
- **Skill Card Tilt:** 3D tilt effect on hover (desktop only, pointer:fine media query)
- **Mobile Nav:** Hamburger toggle with slide-down drawer

---

## CSS Architecture Notes
- All CSS is inline in `<style>` tag (no external stylesheets)
- Sections alternate between `var(--bg)` and `var(--surface)` backgrounds with border separators
- `.reveal` class: transition-based scroll animation (opacity + transform), currently starts visible
- Hero redesigned to match 3D reference portfolio: photo card with tilt, glow orbs, skill chips (all animations restored after `</style>` fix)
- `body::before` (SVG noise texture) and `body::after` (grid pattern) pseudo-elements exist and work now that `</style>` is closed
- Responsive breakpoints: 1024px (hide hero stats), 768px (mobile nav, single-column about, stack photo card), 520px (compact layout, full-width buttons), 480px (contact stack)

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
  index.html          — Main portfolio file (all HTML/CSS/JS, ~1870 lines)
  AGENTS.md           — This context file
  .gitignore          — Ignores OS files, IDE files, .env, node_modules, .vercel
  images/
    profile.jpg       — Hero profile photo
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
  - `Screenshot (242).png` → profile photo (copied to `images/profile.jpg`)
  - `Screenshot (244).png` → OS & Security cert
  - `Screenshot (243).png` → Networking & Cloud cert
  - `Screenshot (246).png` → MERN Stack cert
- Old portfolio history: restored via `git clone https://github.com/ibad2067/portfolio.git`
- Design reference: 3D portfolio (Sushmita Dasari style) — dark ambient glow, photo card, skill chips, Hire Me pill
- Note: A separate Vite/React/Three.js project exists at `Downloads\portfolio` — NOT in use; user chose the old HTML portfolio
