# IdeaX
IdeaX – An AI-powered accessibility platform designed to empower people with disabilities through smart assistive tools, voice commands, speech-to-text in student Laptop, and an easy-to-use interface.
<h1 align="center">🧭 AccessMission</h1>
<p align="center"><b>Your task. Your needs. Your choice.</b></p>
<p align="center">An inclusive campus task planner for persons with disabilities.</p>
<p align="center">
  <img src="https://img.shields.io/badge/HTML5-Structure-orange" alt="HTML5 structure">
  <img src="https://img.shields.io/badge/CSS3-Responsive%20Design-blue" alt="CSS3 responsive design">
  <img src="https://img.shields.io/badge/JavaScript-Rule%20Based%20Planner-yellow" alt="JavaScript rule-based planner">
  <img src="https://img.shields.io/badge/Theme-Inclusive%20Technology-purple" alt="Theme: inclusive technology">
  <img src="https://img.shields.io/badge/MISSION%2726-8%20Hour%20Hackathon-red" alt="MISSION '26 eight-hour hackathon">
</p>

---

##  The Problem

- A person reaches a campus building, but the service they need is upstairs and the lift is unavailable.
- Registration instructions are spoken, while the participant needs written communication.
- A busy location, small text or mouse-only controls make an everyday task harder to complete.
- A location marked “accessible” may still lack a feature that a particular person needs.

**Reaching a place is only one part of completing a task. The route, service and website must work for the person using them.**

##  Our Solution

**AccessMission helps people plan a complete campus task according to their chosen access requirements.**

The user selects a task, such as event registration or library book collection, and chooses the features they need:

-  **No stairs** along the plan.
-  **Written communication** at the service.
-  **A quieter route and service location.**

The planner checks the available sample plans, recommends the quickest matching option and explains its decision.

-  All selected requirements met → show a matching plan.
-  Demo lift unavailable → offer another matching plan, such as a ground-level service.
-  Required feature unconfirmed → exclude that plan and explain why.
-  No plan matches → say so without removing the user's requirements.

##  What Makes It Different

- **Task completion:** considers both the route and the way the service is delivered.
- **Combined requirements:** one person can request several access features together.
- **Alternative service locations:** the same task can be completed through a different matching plan.
- **Explainable decisions:** users can inspect why plans were recommended or excluded.
- **Needs without a diagnosis:** no medical category or account is required.
- **One step at a time:** practice instructions show progress and support Previous, Next and Restart.
- **User-controlled communication:** an editable card helps someone express their request in writing.
- **Offline core:** local files and sample data power the planner without an external API.

Accessibility maps and related services already exist. Our contribution is this task-focused campus demonstration; we do not claim worldwide uniqueness.

##  How the Planner Works

1. Keep candidate plans for the selected task.
2. Check whether each plan's required lift or service is available in the simulation.
3. Require every selected access feature to be explicitly `true`.
4. Record a reason for each failed check.
5. Exclude plans with any failed check.
6. Sort matching plans by their sample estimated time.
7. Recommend the quickest match and allow the user to choose another eligible plan.

| Data value | Meaning | Passes a selected requirement? |
|---|---|---|
| `true` | Feature provided in sample data | Yes |
| `false` | Feature not provided | No |
| `null` or missing | Feature not confirmed | No |

**No AI guesswork. Explicit rules, with explanations for the results.**

##  Accessibility by Design

- Native HTML controls with descriptive labels.
- Keyboard operation and visible focus indicators.
- A skip link to the main content.
- Responsive layout and optional larger text.
- Readable default colours and a higher-contrast mode.
- Screen-reader status announcements for changing results.
- Optional browser text-to-speech, with instructions always available as text.

The application intentionally stores only display preferences in browser storage. Access choices and communication messages are not intentionally persisted.

These features require continued testing with users and assistive technologies. No accessibility certification is claimed.

##  Demo Scenario

1. Choose **Register for MISSION ’26**.
2. Select all three access requirements.
3. Generate the plan: **lift to the quieter event desk — 5 sample minutes**.
4. Turn off **Demo lift available**.
5. Watch the recommendation change to **ground-level registration — 6 sample minutes**.
6. Turn off **Demo ground-level alternatives available**.
7. See a **no matching plan** result, with requirements preserved and exclusions explained.

**The task stays the same; the available way to complete it changes.**

##  Tech Stack

HTML5 · CSS3 · Vanilla JavaScript · Local JavaScript sample data · Browser `localStorage` for display settings · Optional Web Speech API

No framework, backend, database or paid API is required for the prototype.

##  Run It

1. Download or copy the project folder.
2. Keep `index.html`, `styles.css`, `planner.js` and `app.js` together.
3. Open `index.html` in a modern browser.

**No installation or build step is needed.** The core planner works from local files. Optional speech depends on browser/device voice support; preference persistence can vary when using local file URLs.

##  Project Structure

```text
accessmission-starter/
├── index.html          # Page structure, controls and labels
├── styles.css          # Layout, colours and display modes
├── planner.js          # Sample plans and matching rules
├── app.js              # Events, results and practice progress
├── planner.test.cjs    # Decision-rule tests
├── README.md           # Project overview
├── START-HERE.md       # Beginner guide and faculty questions
└── VERIFICATION.md     # Checks performed and remaining limits
```

##  Testing

If Node.js is installed, run:

```bash
node planner.test.cjs
```

The supplied rule tests cover nine targeted scenarios, all 64 combinations of tasks, access requirements and simulated availability, and preservation of the original dataset.

Browser checks also covered keyboard entry, fallback behaviour, no-match results, practice steps, editable messages, display settings and four screen widths. See [VERIFICATION.md](VERIFICATION.md) for details and checks still needed.

##  Prototype Scope

All campus locations, access features, timings and availability are **fictional sample data**. Availability controls affect only this page; they do not report real faults or update other users.

Practice completion does not submit a registration or reserve a book. The prototype does not track physical location or detect obstacles. “No stairs” alone does not establish full wheelchair accessibility.

A real campus pilot would need verified feature information, confirmed alternative services, current availability and testing with people who have relevant access needs.

## 🔮 Future Scope

- Campus-audited routes and service information.
- Authorised staff updates for lift and service availability.
- Sources and last-checked times for access information.
- Additional measured requirements, such as doorway width and rest options.
- Human-reviewed interface translations.
- Integration with actual registration and library services.

##  Team

| Member | Responsibility |
|---|---|
| Jhoshitha.V.L | HTML, content and page structure |
| Yogaratchanaa.N.K | CSS, mobile layout and display design |
| Kamati Lokesh | Sample data and planner rules |
| Harish Kumar.S | JavaScript interactions and integration |
| Rahul.K | Testing and user feedback |
| Praveen.U | Research, documentation and presentation |

##  Learning & Credits

See [START-HERE.md](START-HERE.md) for code explanations, the eight-hour team plan and 24 faculty questions.

This version uses a supplied AI-assisted teaching starter. Document your team's changes and contributions, and follow the event's rules on external resources and generated code.

##  Built For

**MISSION ’26 · 8-Hour Hackathon**

**Theme:** Software Solutions for the Specially Abled — designed around the access needs, dignity and choices of persons with disabilities.
