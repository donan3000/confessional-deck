# Confessional — Presentation Deck

Single-file HTML deck for the 2026-05-04 demo, designed to be opened on the in-world ENGAGE browser.

## Local preview

```bash
cd presentation
python3 -m http.server 8080
# open http://localhost:8080
```

Or just double-click `index.html` — works without a server.

## Navigation (works inside the ENGAGE browser too)

- **Click anywhere** → next slide
- **→ / Space / PageDown** → next slide
- **← / PageUp** → previous slide
- **Home** → first slide, **End** → last slide

The on-screen `← Prev / Next →` buttons are there in case the ENGAGE browser doesn't pass keyboard events.

## Deploying to Cloudflare Pages via GitHub

Target URL: **recovery.kanonindustries.com**

1. **Create a public GitHub repo** (e.g. `confessional-deck`). Push the contents of this `presentation/` folder as the repo root.
2. **Cloudflare Pages → Create project → Connect to Git**, pick the repo.
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
4. Deploy. Cloudflare gives you a `*.pages.dev` URL — verify it works there first.
5. **Custom domain:** Cloudflare Pages → your project → Custom domains → Add Domain → enter `recovery.kanonindustries.com`.
   - If `kanonindustries.com` is on Cloudflare DNS already, Cloudflare adds the CNAME automatically.
   - If not, Cloudflare shows you a CNAME record (`recovery → <project>.pages.dev`) to add manually wherever your DNS lives.
6. Wait ~1–2 min for SSL provisioning. Then `https://recovery.kanonindustries.com` is live.

Every git push auto-deploys. Last-minute slide tweaks → push → live in ~30s.

## Opening it inside ENGAGE

Use the in-world computer / web-browser pane in your confessional location and navigate to the deployed URL. Click anywhere to advance.

## Deck structure (13 slides, academic format)

1. Title
2. §1 The Communication Task
3. §2 Why this scenario?
4. §3 Personas
5. §4 User Stories
6. §5 Requirements (functional + non-functional table)
7. §6 Design Decisions — Atmosphere
8. §7 Design Decisions — Interaction
9. §8 Design Decisions — The AI Agent
10. §9 Team & Collaboration Model
11. §10 Development Tasks
12. §11 Live Demonstration (handoff)
13. §12 References & Discussion

For 5 min, that's ~23s/slide — tight but doable if delivered briskly. If you want more breathing room, request a 7–8 min slot from the instructor or trim §6/§7/§8 into a single combined "Design Decisions" slide.

## Placeholders to fill in before the demo

- **Title slide:** Prof. name (top right)
- **Slide 10 / "Levi":** add Levi's surname in the title slide author line if desired (`Levi · Jonathan Brandes` is currently first-name-then-full-name asymmetric)
- **§10 Development Tasks:** the table groups by area rather than by person; if you want to attribute specific items to one of you, edit the table rows.

## Style notes

- Cream paper background, ink text, deep amber accent. Restrained — university-paper feel rather than pitch-deck.
- Cormorant Garamond (display + italic body) + Inter (body + small caps eyebrows).
- Section markers (§ N) at the top of each content slide; running footer with author line + slide N/13.
- Citations are author-year inline on §1 with full references on §12.

## Design notes

- Palette: deep ink background, candle-amber accent, cream text. Mirrors the room's mood.
- Typography: Cormorant Garamond (serif, contemplative) for display + Inter (clean) for body.
- One small flicker animation in the top-right — keeps the slides feeling alive without distracting.
- 8 slides for ~5 minutes — roughly 35–40s per slide is the right pacing.
