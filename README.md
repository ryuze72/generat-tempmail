# generat-tempmail

Website temporary email + inbox, pakai Theresa API, dengan **backend proxy** agar tidak kena CORS.

## Fitur

- Generate email sementara
- Lihat inbox (auto-refresh)
- Copy email / subject
- Dark modern UI

## API (via proxy)

| Endpoint | Fungsi |
|----------|--------|
| `GET /api/create` | Generate email baru |
| `GET /api/inbox?email=` | Ambil pesan inbox |

Upstream: `https://api.theresav.eu`  
API key disimpan di server (`THERESA_API_KEY` env atau default di proxy).

## Deploy Vercel

1. Import repo `generat-tempmail`
2. (Opsional) set env `THERESA_API_KEY`
3. Deploy

## Lokal

```bash
npx vercel dev
```

Buka http://localhost:3000
