# asiflogic-site

Static site for **asiflogic.net** / **www.asiflogic.net**. Plain HTML/CSS in
[`public/`](./public) — no build step.

## Two ways it is exposed via the Cloudflare surface

Both are driven from the `jldos` repo's `sdf cloudflare` surface
(`sdf.utils.cloudflare_account` holds the shared account facts).

### 1. Cloudflare Workers static assets (edge)

```sh
npx wrangler deploy           # → worker "saladfleet"
```

- Preview: `https://<version>-saladfleet.9jjs2byrwz.workers.dev`
- Production: the `asiflogic.net` / `www.asiflogic.net` custom domains
  (bind them in the dashboard or uncomment the `[[routes]]` in `wrangler.toml`).
- CI deploy: [`.github/workflows/deploy.yml`](./.github/workflows/deploy.yml)
  runs on push to `main` — set the `CLOUDFLARE_API_TOKEN` repo secret
  (Workers Scripts: Edit) to enable it.

### 2. Cloudflared named tunnel (origin on a box)

The durable connector (`sdf cloudflared`) routes `asiflogic.net` →
`http://127.0.0.1:80`. Deploy this repo as that origin with:

```sh
sdf cloudflare site deploy     # clone/pull here + serve public/ on 127.0.0.1:80
sdf cloudflare site status     # unit health + local curl
```

## Account facts

| | |
|---|---|
| account id | `77ba8a9e88f4a4097cf747021de3fa06` |
| zone | `asiflogic.net` |
| worker | `saladfleet` (`*.9jjs2byrwz.workers.dev`) |
| R2 bucket | `jldos` (public: `checkpoint.asiflogic.net`) |
| tunnel id | `06bfd572-fbef-4e28-919c-b4fc058d7f25` |
