# Security policy

## Supported versions

Only the version currently deployed from the `main` branch to https://steve-ndichu.rauell.workers.dev receives security fixes. Older commits, forks and preview builds are not supported.

## Reporting a vulnerability

Use GitHub's private vulnerability reporting: open the repository's **Security** tab and choose **Report a vulnerability** (https://github.com/rauell1/steve-ndichu/security/advisories/new). If that option is not shown, contact the repository owner (GitHub: rauell1) privately. Do not open a public issue, pull request or discussion about a vulnerability.

Please include:

- what you found and where (URL, route, file or commit),
- the steps to reproduce it,
- the impact you expect (for example data exposure or account takeover),
- any proof-of-concept code, screenshots or logs, with personal data removed.

## What to expect

- **Acknowledgement:** within 3 working days.
- **Assessment:** within 10 working days, with a severity rating and next steps.
- **Fix targets:** critical within 7 days, high within 30 days, medium within 60 days, low within 90 days.
- **Credit:** with your permission, you are credited once the fix is released.

## Scope

In scope:

- the production site at https://steve-ndichu.rauell.workers.dev and its API routes,
- the source code and configuration in this repository.

Out of scope:

- vulnerabilities in third-party services this project uses (for example Cloudflare, Neon, Supabase, Resend or GitHub); report those to the provider,
- denial of service, load or volume testing,
- social engineering, phishing or physical attacks,
- missing best-practice headers or reports from automated scanners without a demonstrated impact.

## Safe harbour

Good-faith research that follows this policy is welcome. Do not access, change or delete data that is not yours, do not degrade the service, and stop and report as soon as you reach personal or confidential data. Use test accounts where you can.

## Security practices in this project

- The site is a single static page with no server code, no dependencies and no environment variables or secrets.
- There are no accounts and no forms that store data.
- Deployment credentials (`CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`) live only in GitHub repository secrets.

## For contributors

- Never commit secrets, tokens, connection strings or real personal data. If a secret is committed by mistake, tell the owner at once so it can be rotated; deleting the commit is not enough.
- Add every new environment variable to `.env.example` with a placeholder value, and keep secrets out of variables that reach the browser (`NEXT_PUBLIC_*`, `VITE_*`).
- Treat all request input, webhooks and uploaded files as untrusted.
