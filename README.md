# Good Vibes Coding

Landing page for [goodvibes-coding.com](https://goodvibes-coding.com)

## Stack

- Pure HTML + CSS (no framework, no build step)
- Hosted on [Vercel](https://vercel.com)
- Domain registered through Squarespace
- Email via Google Workspace

## Local Development

Open `index.html` directly in a browser, or start a local server:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`

## Deployment

Deploys automatically to production via Vercel on every push to `main`.

Manual deploy:

```bash
vercel --prod
```

## Project Structure

```
index.html          - Landing page (all sections)
styles.css          - Full stylesheet (OKLCH colors, CSS layers, scroll animations)
team.jpg            - Matt & Melissa team photo (grayscale)
matt.jpg            - Matt headshot (grayscale, not currently used on page)
melissa.jpg         - Melissa headshot (grayscale, not currently used on page)
```

## Infrastructure

| Service            | Provider          | Account                          |
|--------------------|-------------------|----------------------------------|
| Domain             | Squarespace       | goodvibes-coding.com             |
| DNS                | Squarespace       | A record + CNAME to Vercel       |
| Hosting            | Vercel            | zone17s-projects                 |
| Email              | Google Workspace  | hello@goodvibes-coding.com       |
| Email (Matt)       | Google Workspace  | matt@goodvibes-coding.com        |
| Email (Melissa)    | Google Workspace  | mel@goodvibes-coding.com         |

## DNS Records (Squarespace)

| Type  | Name              | Data                                      |
|-------|-------------------|-------------------------------------------|
| A     | @                 | 76.76.21.21 (Vercel)                      |
| CNAME | www               | cname.vercel-dns.com (Vercel)             |
| MX    | @                 | smtp.google.com (Google Workspace)        |
| TXT   | @                 | google-site-verification=... (Google)     |
| TXT   | google._domainkey | v=DKIM1;k=rsa;p=... (DKIM signing)       |

## Contact Info

- Email: hello@goodvibes-coding.com
- Phone: (561) 425-9119
- LinkedIn: linkedin.com/in/mwollsch/
- Website: goodvibes-coding.com

## Team

- **Matt** - AI & Engineering Leadership
- **Melissa** - Business Strategy & Operations

## Strategy & playbooks

Internal business plan, GTM strategy, recipe book, and operations playbooks live in `docs/`. Start here:

- **[Current handoff (2026-05-04)](docs/handoff/2026-05-04-strategy-and-playbooks-handoff.md)** — what state the project is in and what comes next.
- **[Business plan v3 (master)](docs/strategy/2026-04-30-business-plan/23-business-plan-synthesis-v3.md)** — the strategic synthesis. Cold-acquisition motion, dual-geography (Palm Beach + Poconos), three productized starter offerings ($750 / $1,500 / $1,800), $20K MRR target.
- **[Recipe book](docs/strategy/2026-04-30-business-plan/playbooks/01-recipe-book.md)** — what we sell and how to deliver it (9 products, day-by-day build plans).
- **[Operations playbook](docs/strategy/2026-04-30-business-plan/playbooks/02-operations-playbook.md)** — day/week/month rhythms, lifecycle workflows, KPI dashboard.
- **[Claude Code skills library](docs/strategy/2026-04-30-business-plan/playbooks/03-claude-code-skills-library.md)** — installable skills that compound the work (5 starter skills in `playbooks/skills/`).
- **[AI search visibility](docs/strategy/2026-04-30-business-plan/playbooks/04-ai-search-visibility.md)** — top 5 methods for AI search (the technical foundation of the AI Visibility Tune-Up sprint).
- **[PowerPoint deck v3](docs/strategy/2026-04-30-business-plan/deck/GoodVibes-Coding-Business-Plan-v3.pptx)** — the deck.
