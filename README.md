# Stephen Ndichu — Portfolio Website

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
