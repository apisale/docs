# apisale documentation

Developer documentation for [apisale](https://apisale.ai), hosted on [Mintlify](https://mintlify.com).

## Local preview

```bash
cd apisale-docs
npx mintlify dev
```

Open http://localhost:3000 (Mintlify default).

## Deploy

1. Push this folder to GitHub
2. Connect the repo in [Mintlify Dashboard](https://dashboard.mintlify.com)
3. Set custom domain: `docs.apisale.ai`

## Main site integration

Set in `apisale-web`:

```env
NEXT_PUBLIC_DOCS_URL=https://docs.apisale.ai
```

Marketing `/docs` routes redirect to this site.

## Keeping docs in sync

See [docs-sync-design.md](./docs-sync-design.md) for how API and model documentation stay aligned with `apisale-service`.

Quick commands (after sync scripts are added):

```bash
# From repo root — export OpenAPI from NestJS Swagger
npm run docs:export-openapi -w apisale-service

# Validate before deploy
cd apisale-docs && npx mintlify validate
```
