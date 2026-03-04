# AISafe Training Platform — UI Design Prompts
## One prompt per page. Feed directly to Claude to generate production-grade Angular/HTML UI.

---

## MASTER DESIGN SYSTEM (Include at top of EVERY prompt)

```
DESIGN SYSTEM — AISafe Training Platform

Typography:
- Display / Headings: "Sora" (Google Fonts) — geometric, clean, modern. Used by AI-era companies.
- Body: "DM Sans" — readable, neutral, professional. Not overused.
- Mono / Code / Labels: "JetBrains Mono" — technical credibility
- Scale: 12 / 14 / 16 / 20 / 24 / 32 / 40 / 56px

Color Palette (inspired by OpenAI, Anthropic, Notion, Linear):
- Background Primary:   #0A0A0F  (near-black)
- Background Surface:   #111118  (cards, modals)
- Background Elevated:  #18181F  (hover states, sidebars)
- Border Subtle:        rgba(255,255,255,0.06)
- Border Default:       rgba(255,255,255,0.10)
- Text Primary:         #F4F4F5
- Text Secondary:       #A1A1AA
- Text Muted:           #52525B
- Accent Blue:          #3B82F6  (primary CTA — trust, action)
- Accent Blue Hover:    #2563EB
- Accent Green:         #10B981  (success, completion, safe)
- Accent Amber:         #F59E0B  (warning, in-progress)
- Accent Red:           #EF4444  (danger, don't, failure)
- Gradient Hero:        linear-gradient(135deg, #1e3a5f 0%, #0A0A0F 60%)

Fonts: Import Sora, DM Sans, JetBrains Mono from Google Fonts
Spacing: 4px base. Use multiples: 8, 12, 16, 24, 32, 48, 64, 96px
Border radius: 8px default, 12px cards, 16px modals, 9999px pills
Shadows: 0 1px 3px rgba(0,0,0,0.4), 0 8px 32px rgba(0,0,0,0.6)
Motion: 200ms ease micro-interactions, 350ms ease-out page transitions
```

---

## PAGE 1 — Marketing / Landing Page

```
Design a full marketing landing page for "AISafe" — an enterprise AI training & compliance SaaS platform.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Dark, editorial, premium. Like OpenAI's homepage meets Linear's landing page. Confident, not flashy.
The page should feel like it belongs to a company that enterprises trust with compliance.
Use a subtle animated dot-grid or mesh gradient in the hero. Typography does heavy lifting.
Dominant dark theme with precise blue accent moments.

SECTIONS (build all in one HTML file):

1. NAVBAR
   - Logo left: "AISafe" in Sora Bold + inline SVG shield icon
   - Links: Product | Departments | Pricing | Customers | Docs
   - Right: "Request Demo" (solid blue button) + "Sign In" (ghost link)
   - Sticky. Transparent at top → solid #0A0A0F with backdrop-blur after 80px scroll
   - Mobile: hamburger → full-screen overlay menu

2. HERO SECTION
   - Animated background: CSS keyframe moving dot-grid (radial-gradient dots, very subtle movement)
   - Eyebrow: "Enterprise AI Training Platform" — uppercase, letter-spacing: 0.15em, accent blue, 12px
   - H1 (56-64px Sora Bold): "Train Every Team. Secure Every AI Interaction."
   - Subtext (20px DM Sans, #A1A1AA): "Role-based AI safety training for every department. Audit-ready compliance in one platform."
   - CTAs: "Get a Demo" (solid blue, 48px height, rounded-lg) + "See How It Works →" (ghost)
   - Social proof: "Trusted by teams at —" + 5 placeholder company logo rectangles (grey, blurred brand names)
   - RIGHT side visual: CSS-only floating dashboard mockup — stacked cards showing progress bars, "92% complete", certificate icon with blue glow. Cards animate with slight float (CSS keyframe).

3. THE PROBLEM — "The AI Risk Gap"
   - Headline: "Your teams are using AI. Do they know how to do it safely?"
   - 3 stat cards in a row:
     * "73%" — employees use AI without security training
     * "1 in 3" — companies had AI-related data incidents this year
     * "89%" — compliance officers lack visibility into employee AI use
   - Each card: dark bg, thick blue left-border, number in Sora Bold 48px accent blue, description below

4. HOW IT WORKS — 3-step flow
   - Numbered steps connected by animated dashed line (CSS stroke-dashoffset animation)
   - Step 1: Assign by Department (org-chart SVG icon)
   - Step 2: Learn with Scenarios (branching-path SVG icon)
   - Step 3: Prove Compliance (certificate+shield SVG icon)
   - Each step: number circle + title + 2-line description
   - Hover: card lifts slightly, step number glows blue

5. DEPARTMENT TRACKS — "Built for Every Team"
   - Pill tab selector: Engineering | HR | Sales | Finance | Legal | Support | Leadership
   - Clicking a pill shows a content card below (fade + slide transition):
     * Track name, 3 key topics, estimated time badge, one scenario example quote in italic
   - Active pill: blue filled. Inactive: outlined grey.

6. FEATURE BENTO GRID (asymmetric 3-column)
   - Mix large (2-col span) + small (1-col) cards:
     * Large: "Interactive Scenarios" with branching decision tree visual
     * Large: "Audit-Ready Reports" with mini table visual
     * Small x4: Role-Based Tracks | Cheat Sheets | SSO Integration | Certificates
   - Cards: hover → translateY(-4px) + shadow deepens + subtle blue glow

7. TESTIMONIALS
   - "What compliance teams say" heading
   - 3 quote cards: quote | name | title | company placeholder
   - Cards slightly rotated (-1deg, 0deg, +1deg) for organic feel

8. PRICING (3 tiers)
   - Starter / Professional / Enterprise columns
   - Professional highlighted: blue border glow + "Most Popular" badge
   - Feature comparison rows below
   - Enterprise: "Contact Sales" CTA

9. FINAL CTA BAND
   - Full width, gradient background (hero gradient reused)
   - "Ready to close your AI risk gap?" + "Book a Demo" button

10. FOOTER
    - 4 link columns + logo + tagline
    - Trust badges: "SOC2 Ready | ISO 27001 | GDPR Compliant"

INTERACTIONS:
- Navbar transparency → solid on scroll (requestAnimationFrame)
- Stat counter: Intersection Observer triggers count-up animation
- Department pills: CSS transition on content swap
- All cards: 200ms ease hover transform

OUTPUT: Single HTML file. Google Fonts CDN. Vanilla JS only. Production-quality.
```

---

## PAGE 2 — Login / Authentication Page

```
Design a premium login page for "AISafe" enterprise training platform.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Split-screen layout. Left: immersive animated brand panel (45%). Right: precise login form (55%).
Like Linear's auth page — zero decoration on the form side, everything intentional.
The left panel feels alive. The right panel is surgically clean.

LEFT PANEL:
- Background: #0A0A0F → #1e3a5f gradient with 3 animated glowing orbs
  (CSS keyframe: slow drift, 8-12s duration, blur: 80px, opacity: 0.3, colours: blue/indigo/slate)
- Subtle animated grid lines overlay (CSS, opacity: 0.04)
- Centred vertically: AISafe logo (large, white) + tagline "Secure AI Learning for Enterprise Teams"
- Rotating trust stats (JS interval, 4s, fade transition):
  * "173 teams completed AI safety training this month"
  * "Audit-ready reports in one click"
  * "Role-based training for 7 departments"
- Bottom: security badges row — "SOC2" | "ISO 27001" | "256-bit TLS" — small pill badges, semi-transparent white

RIGHT PANEL:
- Background: #0F0F17
- Centred content block (max-width 380px):
  * Small AISafe logo + "Sign in to your workspace" heading (Sora 24px)
  * Email input (48px height, dark bg, blue focus ring via box-shadow)
  * Password input (same height, show/hide toggle eye icon, right side of input)
  * Row: "Remember me" checkbox + "Forgot password?" link (right-aligned, blue)
  * "Sign In" button: full width, 48px, solid blue, Sora semibold, slight glow on hover
  * Divider: thin lines with "or continue with" text centred
  * "Continue with Google" button (Google SVG icon + text, outlined, full width)
  * "Continue with Microsoft" button (Microsoft logo SVG + text, outlined, full width)
  * Bottom footnote: "Don't have an account? Contact your administrator."
  * Micro-text: "By signing in, you agree to Terms and Privacy Policy"

STATES (toggled via small buttons at page top for preview):
1. DEFAULT — as described
2. LOADING — "Sign In" button shows spinner + "Signing in..." text, inputs disabled, opacity 0.6
3. ERROR — Email input: red border + "Invalid email or password" error message below input
4. SUCCESS — Green checkmark replaces button + "Welcome back, Arjun. Redirecting..." text, fade out

FORGOT PASSWORD INLINE FLOW:
- Clicking "Forgot password?" swaps the form content (smooth fade) to:
  * "Reset your password" heading
  * Email input only
  * "Send Reset Link" blue button
  * "← Back to sign in" link
  * No page navigation — pure JS class toggle

DETAILS:
- Input focus ring: box-shadow 0 0 0 3px rgba(59,130,246,0.25)
- Button hover: transform scale(1.01) + box-shadow glow
- All inputs: font-family DM Sans, 16px (prevents iOS zoom)

OUTPUT: Single HTML file. All 4 states + forgot password flow implemented. No framework.
```

---

## PAGE 3 — Learner Dashboard (Home Screen)

```
Design the Learner Dashboard — home screen for employees after login on AISafe.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Clean, motivating, data-forward. Like Duolingo met Linear's UI.
The user always knows what to do next. Progress is celebrated visually.
Green = complete, Blue = in progress, Amber = due soon, Red = overdue.
Generous white space. Cards breathe. No clutter.

LAYOUT: Left sidebar 240px fixed + Main content area fluid

LEFT SIDEBAR:
- Top: Avatar circle (initials "AS", blue bg) + "Arjun Sharma" + "Engineering" dept badge (blue pill)
- Nav items with SVG line icons:
  * 🏠 Home (active: blue left-border + blue text + blue bg tint #3B82F615)
  * 📚 My Learning Path
  * 📋 Cheat Sheets & Resources
  * ✏️ Assessments
  * 🏆 My Certificates
  * 📊 Leaderboard (grey, "Coming Soon" amber badge)
- Bottom: Settings | Help | Sign Out (small, muted)
- Sidebar: background #111118, border-right 1px solid rgba(255,255,255,0.06)

MAIN CONTENT — TOP BAR:
- "Good morning, Arjun. 👋" in Sora 24px
- Subtext: "You have 2 modules to complete before your deadline on March 15." (amber text for urgency)
- Right: notification bell (red dot) + avatar

MAIN BODY (use CSS Grid):

ROW 1 — 4 Stat Cards (equal width):
Card 1: "Modules Completed" — "4 / 9" big number + thin progress bar below (44% filled, blue)
Card 2: "Current Score" — "92%" in green + tiny sparkline SVG (trending up)
Card 3: "Learning Streak" — "🔥 7 Days" in Sora bold + "Keep it up!" sub-text
Card 4: "Deadline In" — "12 Days" in amber (red if <3) + deadline date below
All cards: bg #111118, border rgba(255,255,255,0.08), border-radius 12px, number in Sora bold 32px

ROW 2 — "Continue Learning" (full width, prominent):
- Blue left-border accent (4px solid #3B82F6)
- "In Progress" badge top-right (blue pill)
- Left: module thumbnail (gradient placeholder rectangle 80x60px)
- Content: "Module 3: Safe Prompt Patterns" (Sora 18px) + "Core AI Safety Track" sub-label + progress bar "60% complete" + "~12 min remaining"
- Right: "Continue →" button (solid blue, 40px height)
- Card bg: slight blue tint #3B82F608

ROW 3 — Two columns (60% / 40%):
LEFT — "My Learning Path":
- Section header + "View Full Path →" link
- Vertical list of modules with connector line:
  * ✅ Module 1: What is AI (green check, "Completed Mar 1" timestamp, 95%)
  * ✅ Module 2: Data Privacy (green check, "Completed Mar 3", 88%)
  * → Module 3: Safe Prompt Patterns (blue arrow, "In Progress", progress bar 60%)
  * 🔒 Module 4: Company AI Policy (grey lock, "Unlocks after Module 3")
  * 🔒 Module 5: Recognising AI Content (grey lock)
- Hover rows: bg tint + "Continue" or "Review" action appears

RIGHT — Two stacked cards:
CARD A — "Upcoming Deadline" (amber border-top):
  - "⚠️ Engineering AI Safety Track" + "Due March 15, 2026"
  - "12 days remaining" in amber
  - Progress: "4 of 9 modules complete"
  - "Continue Now →" button (amber outlined)

CARD B — "Saved Resources" (simple):
  - 3 resource rows: [icon] resource name + "Download" icon right
  - "View All Resources →" link

ROW 4 — Leaderboard Preview (subtle, non-intrusive):
- Header: "Engineering Department — This Month"
- Minimal table: rank | name | modules | score — max 5 rows
- Highlight YOUR row: "You — #4" with blue bg tint
- Footer: "Full Leaderboard coming soon"

INTERACTIONS:
- Stat card numbers: count-up from 0 on page load (Intersection Observer)
- Learning path rows: expand with module description on click (smooth max-height transition)
- Sidebar active indicator: smooth slide-left blue bar
- "Continue" card: hover glow + scale(1.01)

OUTPUT: Single HTML file. Sidebar collapsible on mobile. All interactions with vanilla JS.
```

---

## PAGE 4 — Lesson / Module View (Core Learning Experience)

```
Design the Lesson/Module View — the primary learning experience for AISafe.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Immersive and focused. Content is king — the chrome fades away.
Like Masterclass meets enterprise compliance. Premium but purposeful.
When in a scenario, it feels tactile and game-like. When watching video, it's cinematic.
Dark throughout. Progress always visible. Never lost.

LAYOUT: Sticky top progress rail + Two-panel (65% content | 35% outline)

STICKY TOP PROGRESS RAIL:
- Left: "← Dashboard" link (small, muted)
- Centre: "Module 3: Safe Prompt Patterns" | "Lesson 3 of 6" (breadcrumb style)
- Segmented progress bar: 6 equal segments (complete=blue, current=blue pulse animation, upcoming=grey)
- Right: "12 min left" + timer icon

CONTENT PANEL — 4 STATES (show as tab switcher at top for preview):

STATE 1 — VIDEO LESSON:
- Video container (16:9, bg #000, border-radius 12px)
- Custom video controls bar: play/pause | seek bar (blue fill) | 0:00/2:34 | volume | CC | fullscreen
- Above video: "Step 2 of 6 — Core Content" badge (small, muted)
- Below video: lesson title h2 + 2-line description
- "Key Takeaways" expandable card (slides down after video ends):
  * 3 bullet points with blue check icons
  * "Mark Complete & Continue →" button appears here (full width, blue)

STATE 2 — INTERACTIVE SCENARIO:
- Top badge: "What Would You Do?" (amber pill, bold)
- Scenario setup box (bg #18181F, blue left-border, border-radius 8px, padding 20px):
  * Small "📋 Scenario" label
  * Paragraph: "Your colleague Sarah pastes client financial data into ChatGPT to create a summary. She asks you to review before sending. What do you do?"
- 4 choice option cards below:
  * Each: letter badge (A/B/C/D circle) + option text
  * Height: min 64px, padding 16px, border-radius 8px
  * Hover: border-color → #3B82F6, bg tint
  * Selected (pre-submit): blue border + blue bg tint + letter badge fills blue
  * CORRECT (post-submit): green border + green bg tint + "✓ Correct!" badge + explanation text expands below card
  * INCORRECT (post-submit): red border + red tint + "✗ Not quite" + "Here's why..." explanation expands
- "Submit Answer" button (disabled until selection, then solid blue)
- Correct answer toast: "+10 points" badge animates up from bottom, fades after 2s

STATE 3 — DO / DON'T CARD:
- Full-width split card (border-radius 16px, overflow hidden):
  * LEFT HALF (bg #10B98112, border-right 1px solid rgba(255,255,255,0.06)):
    - "✅ DO" header (green, Sora bold 18px)
    - 4 items: green check SVG + text
  * RIGHT HALF (bg #EF444412):
    - "❌ DON'T" header (red, Sora bold 18px)
    - 4 items: red X SVG + text
- Below card: "Save Cheat Sheet" button (outlined, download icon) + "View All Resources" link
- Card feels elevated: box-shadow 0 8px 32px rgba(0,0,0,0.6)

STATE 4 — KNOWLEDGE CHECK:
- Centred card (max-width 640px):
  * "Question 2 of 3" indicator + progress dots row
  * Question text (Sora 20px, line-height 1.6)
  * 4 radio option cards (same style as scenario options but without letter badges)
  * "Next Question →" button
- After all 3 questions → Result:
  * PASS: large "3/3 ✓" in green Sora 56px + "Perfect score! Moving on..." + "Continue →" button
  * PARTIAL: "2/3" in amber + "Good. One question to review." + explanation of missed question + "Retry Quiz" or "Continue" options

LESSON OUTLINE PANEL (right 35%):
- "In This Module" heading (14px uppercase tracking)
- 6 step list items with icons:
  * Video (play-circle icon) — Step 1: Hook
  * Video — Step 2: Core Content (current: blue bg tint + animated blue dot)
  * Scenario (branch icon) — Step 3: Interactive Scenario
  * Card (layers icon) — Step 4: Do / Don't
  * Quiz (pencil icon) — Step 5: Knowledge Check
  * Download (download icon) — Step 6: Resources
- Complete: green check + timestamp + strikethrough text at 0.6 opacity
- Current: blue highlight + "You are here" label
- Future: grey, no interaction
- Time estimates right-aligned (muted)

STICKY BOTTOM NAV BAR:
- Left: "← Previous Step" (ghost)
- Centre: "Step 2 of 6"  
- Right: "Next: Scenario →" (solid blue, disabled until step complete)

INTERACTIONS:
- State tabs: smooth horizontal slide transition (350ms ease-out)
- Scenario option selection: 150ms border color + bg transition
- Answer reveal: card border animates from grey → green/red using CSS transition
- Do/Don't card: items stagger in with opacity animation (100ms delay each)
- Bottom nav "Next" button: scales in from disabled to enabled state

OUTPUT: Single HTML file. 4 states shown via clearly labelled toggle tabs at very top. All interactions.
```

---

## PAGE 5 — Assessment / Final Test

```
Design the Final Assessment page for AISafe — the formal certification exam experience.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Focused, calm-but-serious. A premium exam environment. Reduces anxiety, maintains gravitas.
Like a high-end certification exam platform. Ultra clean. Single column. Nothing competes with the question.
Slightly different background tone (#13131A) signals "exam mode".
Countdown timer is always present but not anxious — calm until it needs to be urgent.

LAYOUT: Centred single column (max-width 720px) on full-screen dark background

PRE-ASSESSMENT SCREEN:
- AISafe logo centred top
- "Final Assessment" heading + "Engineering & IT AI Safety" subtitle
- 4 info cards in 2x2 grid:
  * 15 Questions (question-mark circle icon)
  * 60 Minutes (clock icon)  
  * 80% to Pass (target/bullseye icon)
  * Unlimited Retakes (refresh icon)
- Notice box (amber left-border): key rules as 3 bullet points
- "Start Assessment →" button (full width, 52px, solid blue, Sora semibold)
- "Review modules first" small link below

ASSESSMENT SCREEN:

STICKY TOP BAR:
- "AISafe Assessment" left
- "Question 7 of 15" centre + thin progress bar below (fills proportionally)
- Timer right: "48:32" (blue text) → amber when <10min → red + pulse animation when <5min
- "Exit" link (right, small, clicking shows confirm dialog)

QUESTION CARD (the centrepiece):
- bg #18181F, border-radius 16px, padding 32px, box-shadow deep
- Top row: Question number badge (blue) | Difficulty dots (●●○) | Topic pill ("Data Privacy")
- "🔖 Flag" icon top-right (toggles between outlined/filled amber on click)
- Question text: Sora medium 20px, line-height 1.7, margin-bottom 24px

OPTION TYPES:

MULTIPLE CHOICE:
- 4 cards, each: border-radius 8px, padding 16px 20px, border 1px rgba(255,255,255,0.1)
- Left: letter badge circle (A/B/C/D)
- Option text: DM Sans 16px
- Hover: border → #3B82F6, bg tint
- Selected: filled blue badge + #3B82F620 bg + blue border

SCENARIO QUESTION (same options but with context above):
- Context block: bg #111118, border-left 3px solid #F59E0B, padding 16px, border-radius 0 8px 8px 0
- Small "📋 Scenario" amber label above context text
- Then 4 options as above

TRUE / FALSE:
- Two large side-by-side cards (50/50)
- "✓ True" green tinted card | "✗ False" red tinted card (subtle tint, not garish)

BOTTOM NAVIGATION:
- "← Previous" ghost left
- Question dots centre: filled circle = answered, amber = flagged, current = blue pulse
- "Next →" blue right (or "Review Answers" on Q15)

REVIEW SCREEN (before submit):
- "Review Your Answers" heading
- Scrollable list: each row = Q number | topic | answered ✓ or — | flagged ⚑ | click to jump
- Summary: "15 answered | 3 flagged"
- "Submit Assessment" full-width blue CTA
- "Continue Reviewing" ghost button

RESULTS — PASS (≥80%):
- Tasteful confetti burst (canvas, 2 seconds, blue/green/white particles, then fades)
- SVG circle with score: "93%" drawn with animated stroke (1.5s fill animation), green stroke
- "Assessment Passed!" heading (Sora 32px) + "Excellent work, Arjun."
- Certificate preview card (landscape, looks like real cert): name | course | date | score | verify URL
- "Download Certificate PDF" primary button
- "Share on LinkedIn" secondary button
- Topic score breakdown: mini horizontal bar chart (5 topics, green fill proportional to score)
- "Return to Dashboard" text link

RESULTS — FAIL (<80%):
- Score circle: "64%" amber stroke animation
- "You're Almost There!" heading — supportive, NOT "Failed"
- "You need 80% to pass. Focus on these areas:" 
- 3 weak topic cards: topic name + score + "Review this module →" link
- Progress: "You've improved 8% from your last attempt"
- "Retake Assessment" button with "Available in 23:45:12" countdown (if cooling off)
- "Review Weak Areas" primary button

INTERACTIONS:
- Timer: live JS countdown, colour transitions via class toggle
- Question slide: horizontal translate (like Tinder swipe but subtle, CSS transition)
- Option selection: instant 150ms feedback
- Flag toggle: bookmark fill animation
- Score circle: SVG stroke-dashoffset animation on result reveal
- Confetti: requestAnimationFrame canvas particles

OUTPUT: Single HTML file. Buttons to toggle between all screens (Pre | Question | Scenario Q | Review | Pass | Fail).
```

---

## PAGE 6 — Admin Dashboard

```
Design the Admin Dashboard for AISafe — command centre for compliance & L&D administrators.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Data-dense but never overwhelming. Like Linear's project dashboard or Vercel's analytics.
Admins see problems instantly and act in 2 clicks. Numbers are heroes.
Green/amber/red used purposefully for compliance health. Trusted, professional, sharp.
Inspired by: Datadog, Linear, Vercel dashboards.

LAYOUT: Sidebar 240px + Main content area

SIDEBAR (admin version):
- Logo top
- Nav: Overview (active) | Users & Groups | Assign Training | Content Manager | Assessments | Reports | Settings
- "Switch to Learner View" small link at bottom (with user icon)

MAIN TOP BAR:
- "Overview" page title (Sora 24px)
- Right: "Acme Corp" tenant badge + "Last 30 days ▼" date filter + "Export Report" button (outlined) + bell + avatar

BODY GRID:

ROW 1 — 5 KPI Cards:
1. "Overall Completion" — "67%" large + SVG donut chart (67% blue, 33% dark) + "↑ 8% vs last month" green
2. "Active Learners" — "342 / 512" + progress bar + "67% of company"
3. "Overdue Users" — "47" in red Sora bold + "↑ 12 new this week" small red text — red bg tint on this card
4. "Avg. Assessment Score" — "84%" green + "↑ 3pts" trend
5. "Certificates Issued" — "289 this month" blue + calendar icon

ROW 2 — 60/40 columns:

LEFT — "Completion by Department" table:
- Header row: Department | Progress | Completion % | Status | Action
- 7 data rows:
  * Engineering: progress bar 78% green | "78%" | "On Track" green badge | "View →"
  * HR: progress bar 91% green | "91%" | "On Track" | "View →"
  * Sales: progress bar 54% amber | "54%" | "At Risk" amber badge | "View →"
  * Finance: progress bar 82% green | "82%" | "On Track" | "View →"
  * Legal: progress bar 38% red | "38%" | "Critical" red badge | "Remind →" (action changes)
  * Support: progress bar 69% amber | "69%" | "At Risk" | "View →"
  * Leadership: progress bar 95% green | "95%" | "On Track" | "View →"
- Row hover: bg tint + cursor pointer

RIGHT — Risk Maturity Score card:
- "AI Risk Maturity by Department" heading + "?" tooltip icon
- Radar/spider chart using Chart.js:
  * 7 axes: Engineering/HR/Sales/Finance/Legal/Support/Leadership
  * Current scores polygon: blue, 60% opacity
  * Target polygon: green outline only
- Legend: "● Current (avg 71)" "○ Target (85)"
- "Learn how scores are calculated →" link

ROW 3 — Three equal columns:

COL 1 — "Overdue Users" (red top-border accent):
- "⚠️ 47 Users Overdue" heading in red
- 5 rows: avatar circle + Name + dept + "X days overdue" (more days = more red intensity)
- "Remind All Overdue" button (amber, outlined, full width)
- "View Full List →" link

COL 2 — "Activity Feed":
- Scrollable (max-height: 300px, custom scrollbar)
- Timestamped events with colour dots:
  * 🟢 "Sarah M. completed Engineering Final Assessment (97%)" — 2h ago
  * 🔵 "New user: james.w@acme.com added via SSO" — 3h ago
  * 🟡 "Deadline reminder sent to Legal dept (38 users)" — 5h ago
  * 🔴 "Tom K. failed assessment (62%) — 3rd attempt" — Yesterday
  * (8+ events total)

COL 3 — "Quick Actions":
- 4 full-width action buttons, each with left icon:
  * "＋ Add Users" (solid blue)
  * "🔔 Send Reminders to Overdue" (amber outlined)
  * "📊 Generate Audit Report" (ghost)
  * "📚 Assign New Training" (ghost)
- Hover: blue bg tint on all

ROW 4 — Assessment Analytics (full width):
- "Quiz Performance by Department" heading + date range right
- Chart.js grouped bar chart:
  * X-axis: 7 departments
  * 3 bar groups per dept: Avg Score | Pass Rate | 1st Attempt Pass
  * Y-axis: 0-100%
  * Tooltips on hover
- Below chart: small table "Lessons with highest failure rate": lesson name | dept | failure % | "Review content" link

ROW 5 — Upcoming Deadlines (full width):
- "Upcoming Deadlines" heading
- Horizontal scrollable card row:
  * Each card: assignment name | dept | due date | "X days" | completion % so far | coloured by urgency
  * Overdue: red border | <7 days: amber border | comfortable: grey border
- "Manage All Deadlines →" link

INTERACTIONS:
- KPI card numbers: count-up on load
- Donut chart + radar chart: animate in on page load
- Bar chart: bars grow from bottom (staggered 50ms per bar)
- Table rows: hover row highlight + action appears
- Overdue user list: hover shows "Send Reminder" button inline

OUTPUT: Single HTML file. Chart.js from CDN. All data as realistic hardcoded dummy values. Mobile: sidebar collapses.
```

---

## PAGE 7 — User Management (Admin)

```
Design the User Management page for AISafe admin panel.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Clean, efficient data table. Like Stripe's customer table or Linear's issue list.
Every row is an action surface. Bulk operations are first-class. Search is instant.
Dark theme. Table rows breathe. Status colour-coded at a glance.
Inspired by: Stripe Dashboard, Airtable, GitHub user management.

LAYOUT: Full-width within existing admin shell

PAGE HEADER:
- "Users & Groups" title (Sora 24px)
- Tabs: "All Users (512)" | "Groups (14)" | "Departments (7)" | "Import Log"
- Right: "Import CSV" (outlined) | "Add User" (solid blue) | "Sync from SSO" (ghost, refresh icon)

FILTER BAR:
- Search: full-width input with search icon, "Search name, email, department..." placeholder
  * Instant filter, 150ms debounce
- Second row — filter pills:
  * Department ▼ (dropdown multi-select)
  * Status: All | Active | Inactive
  * Training: All | On Track | Overdue | Not Started | Complete
  * Role: All | Admin | Learner | Manager
- Active filters as removable pills ("Engineering ×", "Overdue ×")
- Right: "Showing 47 of 512" count + "Bulk Actions ▼" dropdown

USERS TABLE:
Headers (sortable, click = sort arrow):
☐ | Name / Email | Department | Role | Status | Training Progress | Last Active | Actions

Rows (show 8 sample rows):
- ☐ checkbox
- Avatar (initials circle, dept colour) + "Arjun Sharma" bold + "arjun.s@acme.com" muted small
- "Engineering" dept badge (blue pill)
- "Learner" or "Admin" role badge
- Green "●Active" / Grey "●Inactive" dot + text
- Mini progress bar (40px) + "4/9" small + status colour indicator
- "2 days ago" relative time
- "···" kebab (hover reveals) → View | Assign | Remind | Deactivate

ROW STATES:
- Default: normal
- Hover: subtle bg tint (#ffffff04)
- Overdue: amber left-border (2px)
- Selected: blue bg tint + checkbox filled
- Inactive: 50% opacity

BULK ACTION BAR (appears at bottom when rows selected):
- Fixed bottom, full width, slides up from -60px with spring animation
- bg #1e3a5f, border-top blue
- "47 users selected" | Assign Training | Send Reminder | Export CSV | Deactivate | ✕ Clear selection

USER DETAIL SIDE DRAWER (480px, slides from right):
- Show as pre-opened for preview
- User header: large avatar + Name + email + dept badge + status + "Edit Profile" button
- Tabs: Overview | Training | Certificates | Activity
- Overview tab content:
  * Info grid: Department | Role | Location | Manager | Member Since | Last Login
  * Stats row: Modules Completed (6) | Avg Score (88%) | Certs Earned (1)
- Training tab: list of assigned courses with status indicators + "Assign More +" button
- Backdrop: main content dims to 30% opacity when drawer open

IMPORT CSV MODAL (full-screen overlay, stepped):
- Step indicator at top: 1 Upload → 2 Map Fields → 3 Validate → 4 Confirm
- Step 1: Drag-and-drop zone (dashed border 2px, upload cloud icon, "or browse files", accepted: .csv .xlsx)
  * "Download sample CSV template" link
- Step 2: Field mapping — 2-column layout: "Your CSV Column" → (dropdown) → "AISafe Field"
  * 6 field rows with select dropdowns
- Step 3: Validation — "✓ 509 valid rows | ⚠ 3 errors" + error detail table
- Step 4: Preview 5 rows + "Import 512 Users" CTA button

PAGINATION:
- "← Prev" | 1 2 3 … 12 | "Next →"
- "25 per page ▼" selector
- Smooth table transition between pages

INTERACTIONS:
- Search: live table filter (JS Array.filter on dummy data)
- Column sort: click header → sort with visual indicator
- Bulk bar: spring animation (translateY)
- Drawer: 350ms slide-in + backdrop fade
- Import modal: step progression with horizontal slide
- Kebab menu: dropdown with smooth opacity

OUTPUT: Single HTML file. Pre-populate with 8-10 realistic dummy user rows. Drawer pre-open for preview.
```

---

## PAGE 8 — Cheat Sheets & Resources Library

```
Design the Cheat Sheets & Resources Library for AISafe learners.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Warm, organised, like a premium reference library. Cards feel tactile — like physical reference cards.
Not cold or clinical. A learner should feel: "Everything I need is right here, within reach."
Dark theme with slightly warmer card backgrounds. Bookmarking is satisfying.
Inspired by: Raindrop.io, Notion gallery view, premium knowledge bases.

PAGE HEADER:
- "Cheat Sheets & Resources" title (Sora 28px)
- "Your personal AI safety reference library." subtitle (muted)
- Right: search bar + "Filter ▼" + grid/list view toggle icons

CATEGORY TABS (horizontal scrollable):
"All (34)" | "Prompt Templates (8)" | "Do/Don't Cards (12)" | "Checklists (7)" | "Redaction Examples (5)" | "Policy Summaries (2)"
Active: blue underline + blue text. Others: grey text.

RESOURCE GRID (3 columns, responsive):

CARD TYPES:

DO/DON'T CARD:
- Top: "Do / Don't" amber pill badge + department tag (e.g. "Engineering")
- Card title: "AI Tool Usage — Engineering Team"
- Mini preview strip (inside card):
  * Left: green bg strip — 2 short ✓ items  
  * Right: red bg strip — 2 short ✗ items
- Footer: "Updated Mar 2026" | bookmark icon (outlined/filled toggle) | download icon | preview eye icon

PROMPT TEMPLATE CARD:
- Top: "Prompt Template" blue pill badge
- Card title: "Safe Data Analysis Prompt"
- Code-block preview (bg #0A0A0F, mono font, 12px):
  "You are a data analyst. Analyse [DATA] for trends. Do not include personal..."
  Text fades with bottom gradient
- Footer: same actions as above

CHECKLIST CARD:
- Top: "Verification Checklist" green pill badge  
- Card title: "Pre-Submit AI Output Checklist"
- Preview: 3 checkbox rows (2 checked, 1 unchecked)
  * ☑ Checked for PII in the prompt
  * ☑ Verified source information
  * ☐ Cross-referenced with official docs
- Footer: same actions

ALL CARDS:
- bg #18181F with very subtle type-specific gradient tint (blue for prompts, green-ish for checklists)
- border 1px rgba(255,255,255,0.08)
- border-radius 12px
- Hover: translateY(-4px), shadow deepens, border-color brightens
- "Updated" amber badge if content updated since last view
- Bookmarked cards: bookmark icon fills amber instantly on click (satisfying toggle)

RESOURCE PREVIEW MODAL (full-screen overlay on card click):
- Dark overlay bg-#0A0A0FE8 with blur
- Centred modal: max-width 800px, bg #111118, border-radius 16px
- Top: title + type badge + "⬇ Download PDF" + "✕ Close"
- Body renders full resource:
  * DO/DON'T: full two-column split layout at readable size
  * PROMPT: full mono text block with "📋 Copy" button top-right of code block
  * CHECKLIST: interactive checkboxes (check state saves to memory)
- Bottom: "Related Resources" — 3 mini card row
- Close on ESC or backdrop click

UPDATED NOTICE:
- Cards updated after user's last visit: amber "Updated" badge + tooltip "Updated Mar 5 — what changed →"

EMPTY STATE (no saved bookmarks filter):
- SVG shield + bookmark illustration (simple, line-art)
- "No saved resources yet"
- "Save cheat sheets at the end of each lesson"
- "Browse All →" CTA

INTERACTIONS:
- Bookmark toggle: heart-like scale animation (1 → 1.3 → 1), icon fills amber
- Card hover: 200ms translateY + shadow
- Category tab switch: content grid fades and reloads (opacity transition)
- Modal: scale from 0.95 + opacity 0 → 1 (250ms)
- Checklist checkboxes: animated checkmark draw (SVG stroke animation)

OUTPUT: Single HTML file. Modal pre-open for preview. Bookmark states toggle via JS. Realistic content.
```

---

## PAGE 9 — Certificates & Achievements (Learner)

```
Design the Certificate & Achievements page for AISafe learners — their trophy room.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Celebratory but professional. This is the "reward" page. Make the learner feel proud.
Certificates must look premium enough to share on LinkedIn.
Warm gold/blue accents on dark. Like a digital award ceremony.
Achievement badges feel collectible like Pokémon meets enterprise creds.
Inspired by: Credly, Apple Wallet, Masterclass certificates.

LAYOUT: Single column, centred (max-width 900px), generous padding

SECTION 1 — CERTIFICATES:

"My Certificates" heading + "3 earned" blue badge

Certificate selector (if 3 certs): horizontal row of 3 thumbnail cards
- Each: small cert preview + course name + date + check icon
- Active: blue border highlight

LARGE CERTIFICATE (the centrepiece — full CSS, no image):
Container: 760px × 427px (16:9), centred
Design:
- Background: #0D1B3E (deep navy) with CSS geometric line pattern (subtle, low opacity lines crossing)
- Thin outer border: 2px solid rgba(201,168,76,0.5) — muted gold
- Inner padding: 48px
- TOP SECTION:
  * "AISafe" logo centred (SVG, white wordmark + small shield)
  * Thin horizontal rule: linear-gradient(90deg, transparent, #C9A84C, transparent) height 1px
  * "CERTIFICATE OF COMPLETION" in Sora 10px, letter-spacing: 0.25em, #C9A84C uppercase
  * Thin rule again
- CENTRE:
  * "This certifies that" in DM Sans italic 14px, #A1A1AA
  * Learner Name: Sora Bold 36px, #F4F4F5 — "Arjun Sharma"
  * "has successfully completed" DM Sans 14px, #A1A1AA
  * Course Name: Sora SemiBold 22px, #3B82F6 — "Engineering & IT AI Safety Training"
  * "with a score of 93% on March 4, 2026" — DM Sans 14px, #A1A1AA
- BOTTOM ROW (3 columns):
  * "Score: 93%" left
  * AISafe shield icon centre (slightly larger, with subtle glow)
  * "ID: AS-2026-0847" right (JetBrains Mono 11px)
- VERY BOTTOM: "Verify at verify.aisafe.io/AS-2026-0847" JetBrains Mono 10px, muted
- Corner ornaments: thin CSS geometric corners at all 4 corners (gold colour)

ACTION BUTTONS ROW (below certificate):
- "⬇ Download PDF" (solid blue, 44px)
- "💼 Share on LinkedIn" (LinkedIn blue #0077B5, outlined)
- "🔗 Copy Verification URL" (ghost)
- "🖨 Print" (ghost)
- All inline, centred

VERIFICATION BADGE (small card below buttons):
- "✓ Verified Certificate" green check + "Valid as of March 2026"
- "Independently verifiable by employers and auditors — no account needed"

SECTION 2 — ACHIEVEMENTS:

"Badges & Achievements" heading (Sora 22px) + "5 earned, 3 locked" muted sub-count

4-column grid of badge cards:

EARNED BADGES (bright):
- "AI Safety Foundation" — shield SVG, blue gradient, glow on hover
- "Prompt Safety Expert" — terminal/code SVG, green gradient
- "Data Privacy Champion" — lock SVG, amber gradient
- "Zero Incidents" — flame SVG, orange gradient
- "Speed Learner" — lightning bolt SVG, yellow

LOCKED BADGES (greyed out):
- "Department Champion" — trophy SVG, 40% opacity, padlock overlay on icon
- "Perfect Score" — star SVG, locked
- "Early Adopter" — rocket SVG, locked

Each badge card:
- Circular icon container (80px diameter) centred on card
- Badge name (Sora 13px) below
- Earned: "Earned Mar 4, 2026" green text small
- Locked: "Lock" grey text + "How to earn: Complete all modules with 90%+" tooltip on hover
- Hover (earned): scale(1.08) + glow intensifies
- Hover (locked): shake animation + tooltip shows requirement

LINKEDIN SHARE MODAL (shown via "Share on LinkedIn" button):
- Overlay with LinkedIn mockup preview
- Shows post with certificate image + pre-written caption:
  "I've completed the Engineering AI Safety Training on AISafe Platform, achieving 93%. #AISafety #AILiteracy"
- Editable caption text area
- "Open LinkedIn →" blue button (LinkedIn branded)
- Footnote: "This opens LinkedIn with pre-filled content for you to post"

INTERACTIONS:
- Certificate selector: smooth crossfade between certs (opacity transition)
- Earned badge hover: scale + SVG glow pulse
- Locked badge click: shake animation (translateX 0→3px→-3px→0, 300ms)
- Copy URL button: instant "Copied! ✓" state (2s then resets)
- Download: brief "Generating PDF..." state → "Downloaded ✓"
- LinkedIn modal: backdrop blur + modal scale-in

OUTPUT: Single HTML file. Certificate as pure CSS/HTML. All badge states visible. Modal shown pre-open.
```

---

## PAGE 10 — Reports & Audit Export (Admin)

```
Design the Reports & Audit Export page for AISafe admin panel.

[PASTE DESIGN SYSTEM ABOVE]

AESTHETIC DIRECTION:
Serious, trust-inducing, precision. Used when a compliance officer needs evidence for an audit.
Everything communicates reliability, traceability, control. Like Bloomberg meets accessible enterprise.
No decorative elements — data and actions only. But still polished and branded.
Dark theme. Export actions prominent. Tables feel solid and trustworthy.
Inspired by: Stripe Reporting, Datadog, Workday compliance reporting.

LAYOUT: Left report type panel (260px) + Right report builder area (fluid)

LEFT PANEL — "Report Templates":
- Header: "Report Templates"
- Grouped list:
  GROUP "Completion":
    * 📊 Company Completion Summary — "CSV + PDF"
    * 🏢 Department Breakdown — "CSV + PDF" (ACTIVE)
    * 👤 Individual User Completion — "CSV"
    * ⚠️ Overdue Users — "CSV + PDF"
  GROUP "Assessment":
    * 📈 Score Distribution — "CSV + PDF"
    * ❌ Question Failure Analysis — "CSV"
    * 🔄 Retake History — "CSV"
  GROUP "Compliance / Audit":
    * ✅ Policy Acknowledgement Log — "PDF"
    * 🏆 Certificate Audit Trail — "PDF"
    * 📋 Content Version Log — "CSV"
    * 📦 Full Audit Export — "ZIP" (gold badge: "Audit-Ready")
  GROUP "Custom":
    * ➕ Build Custom Report
- Active item: blue left-border + blue text + blue bg tint
- Group headers: uppercase 11px, letter-spacing 0.1em, muted text

RIGHT AREA:

HEADER:
- "Department Completion Breakdown" title (Sora 24px) + pencil edit icon
- Breadcrumb: Reports / Completion / Department Breakdown
- Right: "⏰ Schedule Report" (ghost) + "Generate Report" (solid blue, prominent)

FILTER CARD ("Report Parameters"):
- Date Range: "From [date picker] To [date picker]" + preset buttons: "7D | 30D | Quarter | Year | Custom"
- Departments: multi-select checkboxes (all checked by default) in 2-column layout
- Training Tracks: toggle chips: All | Core | Role-Based | Refreshers
- Include Fields: checkboxes: Completion % | Scores | Time Spent | Cert Status | Policy Acks | Dept Avg
- Group By: radio: Department | Location | Role | Custom Group
- "Apply Filters" button right-aligned

PREVIEW TABLE (below filters):
- "Preview (first 10 rows)" label + "↻ Refresh" icon
- Dark table, sticky headers
- Columns: Department | Users Assigned | Completed | In Progress | Not Started | Avg Score | Completion % | Status
- 7 data rows (one per dept) — realistic data
- Amber left-border rows for overdue departments
- Status column: colour-coded badge (On Track green, At Risk amber, Critical red)
- Totals row at bottom: slightly different bg
- "Showing 10 of 7 departments. Full export includes all records." footnote

EXPORT SECTION:
- "Export Full Report" heading (Sora 18px)
- Format cards (3 toggle-select cards):
  * "CSV" (table icon) — "For Excel / Google Sheets analysis"
  * "PDF" (document icon) — "Formatted, branded, audit-ready" — SELECTED with blue border
  * "Both" (both icons) — "Download as ZIP"
- Expandable "Export Options" panel:
  * Checkboxes: Include company logo | Add watermark | Include cover page | Add admin signature line | Include generation metadata
- "Generate & Download" CTA (full width, 52px, solid blue, Sora semibold)
- LOADING STATE: "Preparing your report... 67%" with animated progress bar
- SUCCESS STATE: "✓ Report ready — downloading..." green confirmation

SCHEDULE REPORT MODAL:
- "Schedule This Report" modal
- Frequency: Daily | Weekly | Monthly toggle
- Send to: email input (multi-value chips)
- Format: CSV / PDF toggle
- "Create Schedule" CTA

EVIDENCE TRAIL SECTION:
- Collapsible card: "Evidence Trail — Compliance Data" + ▼ toggle
- If expanded: 3 sub-tabs: Policy Acknowledgements | Content Versions | Completion Timestamps
- Each tab: table with timestamp | user | action | content version | status
- Green shield badge: "All records are immutable and cryptographically signed"
- "Export Evidence Package (ZIP)" button

REPORT METADATA FOOTER (always visible at bottom of preview):
- Subtle bg #18181F, border-top
- "Report generated by: admin@acme.com | March 4, 2026 14:32 UTC | AISafe Platform v2.1 | Tenant: Acme Corp"
- Mono font, small, muted

INTERACTIONS:
- Left panel click: smooth right area content transition (fade + slight slide)
- Filter changes: table shows loading shimmer → new data
- Format card selection: border animation, bg tint
- Generate button: progress bar animation → success state
- Schedule modal: slides up (mobile sheet behaviour)
- Evidence trail expand: smooth max-height animation

OUTPUT: Single HTML file. Chart.js for any charts. All states toggled for preview. Realistic dummy data.
```

---

## DESIGN TOKENS (CSS Variables — Share with Angular Dev)

```css
/* AISafe Design System — design-tokens.css */
/* Import in Angular: styles.scss */
/* @import url('design-tokens.css'); */

@import url('https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700;800&family=DM+Sans:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap');

:root {
  /* Backgrounds */
  --bg-base: #0A0A0F;
  --bg-surface: #111118;
  --bg-elevated: #18181F;
  --bg-overlay: rgba(0, 0, 0, 0.75);

  /* Borders */
  --border-subtle: rgba(255, 255, 255, 0.06);
  --border-default: rgba(255, 255, 255, 0.10);
  --border-strong: rgba(255, 255, 255, 0.20);

  /* Text */
  --text-primary: #F4F4F5;
  --text-secondary: #A1A1AA;
  --text-muted: #52525B;
  --text-inverse: #09090B;

  /* Accent — Blue */
  --blue: #3B82F6;
  --blue-hover: #2563EB;
  --blue-muted: rgba(59, 130, 246, 0.12);
  --blue-glow: 0 0 40px rgba(59, 130, 246, 0.2);

  /* Accent — Green (success, complete, safe) */
  --green: #10B981;
  --green-muted: rgba(16, 185, 129, 0.12);

  /* Accent — Amber (warning, in-progress, due soon) */
  --amber: #F59E0B;
  --amber-muted: rgba(245, 158, 11, 0.12);

  /* Accent — Red (danger, don't, overdue) */
  --red: #EF4444;
  --red-muted: rgba(239, 68, 68, 0.12);

  /* Gold (certificates) */
  --gold: #C9A84C;
  --gold-muted: rgba(201, 168, 76, 0.15);

  /* Department Colours */
  --dept-engineering: #3B82F6;
  --dept-hr: #8B5CF6;
  --dept-sales: #10B981;
  --dept-finance: #F59E0B;
  --dept-legal: #6366F1;
  --dept-support: #EC4899;
  --dept-leadership: #14B8A6;

  /* Typography */
  --font-display: 'Sora', sans-serif;
  --font-body: 'DM Sans', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  /* Font Sizes */
  --text-xs: 11px; --text-sm: 13px; --text-base: 15px;
  --text-md: 17px; --text-lg: 20px; --text-xl: 24px;
  --text-2xl: 30px; --text-3xl: 38px; --text-4xl: 48px; --text-5xl: 60px;

  /* Spacing */
  --s1: 4px; --s2: 8px; --s3: 12px; --s4: 16px; --s5: 20px;
  --s6: 24px; --s8: 32px; --s10: 40px; --s12: 48px; --s16: 64px; --s24: 96px;

  /* Border Radius */
  --r-sm: 6px; --r-md: 8px; --r-lg: 12px;
  --r-xl: 16px; --r-2xl: 20px; --r-full: 9999px;

  /* Shadows */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.4);
  --shadow-md: 0 4px 16px rgba(0,0,0,0.5);
  --shadow-lg: 0 8px 32px rgba(0,0,0,0.6);
  --shadow-xl: 0 16px 64px rgba(0,0,0,0.7);

  /* Motion */
  --dur-fast: 150ms;
  --dur-normal: 200ms;
  --dur-slow: 350ms;
  --ease-default: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
}
```

---

*10 page prompts + Master Design System + Design Tokens*
*Pages: Landing | Login | Learner Dashboard | Lesson View | Assessment | Admin Dashboard | User Management | Resources Library | Certificates | Reports*
*Always include the DESIGN SYSTEM block at the top of every prompt when generating pages.*
