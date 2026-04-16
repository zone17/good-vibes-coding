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
