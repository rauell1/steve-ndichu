# Stephen Ndichu portfolio website

A responsive, single-page portfolio website for Stephen Ndichu, a commercial leader and electric mobility specialist based in Nairobi, Kenya.

## Tech stack

- Semantic HTML5
- CSS and vanilla JavaScript embedded in `index.html`
- Google Fonts
- No framework, package manager, or build step required

## Run locally

Open `public/index.html` directly in a browser, or serve the project directory with any static web server. For example:

```bash
npx serve public
```

## Deploy to Cloudflare

The site is served by Cloudflare Workers static assets. `wrangler.jsonc` points at the `public/` directory and attaches the `steve-ndichu.rauell.systems` custom domain.

Every push to `main` runs `.github/workflows/deploy-cloudflare.yml`, which deploys with Wrangler. The workflow needs two repository secrets:

- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`

To preview locally:

```bash
npx wrangler dev
```

## Project structure

```text
.
├── public/
│   └── index.html   # Complete portfolio site
├── wrangler.jsonc   # Cloudflare Workers configuration
└── README.md        # Project documentation
```

## Repository

[github.com/rauell1/steve-ndichu](https://github.com/rauell1/steve-ndichu)

## Project information

| | |
|---|---|
| Live site | https://steve-ndichu.rauell.workers.dev |
| Hosting | Cloudflare Workers |
| Default branch | `main` |
| Repository | Public |

### Stack

- Semantic HTML5 with embedded CSS and vanilla JavaScript (`public/index.html`)
- Cloudflare Workers static assets

### Deployment

Production runs on Cloudflare Workers at https://steve-ndichu.rauell.workers.dev. `.github/workflows/deploy-cloudflare.yml` builds and deploys on every push to `main`, using the `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` repository secrets. Public build-time values are repository variables; runtime secrets are Worker secrets.

### Contributing and security

- How to set up, test and submit changes: [CONTRIBUTING.md](CONTRIBUTING.md)
- How to report a vulnerability: [SECURITY.md](SECURITY.md)
- Expected behaviour in project spaces: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

### Licence

No open-source licence has been granted. The code, content and brand assets belong to the project owner and all rights are reserved. Ask the owner before reusing any part of this repository.
