# Nushir documentation

Source for [docs.nushir.com](https://docs.nushir.com), built with
[Mintlify](https://mintlify.com). Pushing to `main` deploys.

## Layout

| Path | What |
|---|---|
| `docs.json` | Navigation, theme, branding |
| `index.mdx` | Landing page |
| `guide/` | Product guide |
| `channels/` | Per-platform reference |
| `api-reference/` | API pages plus `openapi.yaml` |
| `logo/`, `favicon.png` | Brand assets |

## The API reference is generated

`api-reference/openapi.yaml` describes the real
`/public/v1` surface, derived from `public.integrations.controller.ts` in the
application. Mintlify renders one page per endpoint from it — do not hand-write
endpoint pages, extend the spec instead.

When the controller changes, update the spec in the same change.

## Local preview

```bash
npm i -g mint
mint dev
```
