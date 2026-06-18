# Parking Zero / Park Go Recife

## Cloudflare Pages

Use Cloudflare Pages Git integration with these settings:

- Build command: `npm run build`
- Build output directory: `dist`
- Deploy command: `npm run deploy:cloudflare:ci`
- Node version: `22.12.0` or newer

Do not use `/` or `npx wrangler deploy` as a deploy command for Pages. `/` is treated as a
shell command and fails with `Permission denied`; `npx wrangler deploy` targets Workers and
triggers Wrangler's interactive TanStack setup.

If you want to deploy manually from a local terminal, use:

```bash
npm run deploy:cloudflare
```

Required environment variables:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`
- `SUPABASE_URL`
- `SUPABASE_PUBLISHABLE_KEY`
