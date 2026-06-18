---
name: start
description: Sätt upp och bygg projektet steg för steg — plan, scaffold, databas (Supabase), deploy (Vercel), git. Kör detta först i ett nytt projekt.
---

# /start — från noll till live

Du guidar en ICKE-TEKNISK medlem som bygger "Recensionsroboten". Var pedagogisk,
förklara på svenska, och be ALLTID om godkännande (ja/nej) före något som kostar
pengar eller publicerar. Echo:a ALDRIG hemligheter/nycklar i chatten.

## Steg 0 — Förkrav
- Kör `git --version` och `node --version`. Saknas något: be användaren installera det och stanna.
- Be användaren köra `/mcp` och logga in på **supabase**, **vercel**, **github** (webb-inloggning, inga nycklar). Vänta tills klart.
- Läs `/affarsplan` för att förstå vad vi bygger.

## Steg 1 — Plan
Föreslå en konkret 4–6-stegs MVP-plan utifrån /affarsplan. Vänta på OK innan du bygger.

## Steg 2 — Scaffold (kostar inget)
Bygg grunden (Next.js + Tailwind om den inte finns). Kör `npm run dev` och visa att appen startar.

## Steg 3 — Databas (Supabase) — kostar pengar
- Skapa projekt via Supabase-MCP (`create_project`). **Visa kostnaden och be om ja/nej** (`confirm_cost`).
- Skapa tabeller med `apply_migration`. Generera typer med `generate_typescript_types`.
- Hämta publika nycklar med `get_publishable_keys` och skriv dem till `.env.local` (echo:a dem ALDRIG).
- Uppdatera `.mcp.json` med projektets `project_ref`.

## Steg 4 — Spara i git
`git add . && git commit -m "..." && git push`.

## Steg 5 — Publicera (Vercel) — be om ja/nej först
- Via Vercel-MCP: koppla repot, sätt env-variabler (från `.env.local`), deploya.
- Visa den live URL:en för användaren och fira. 🎉

## Steg 6 — Om appen behöver Claude API
Be användaren skapa en nyckel på console.anthropic.com → Create Key, klistra in EN gång.
Skriv den till `.env.local` (echo:a den aldrig).

## Hela tiden
- Uppdatera `docs/FRAMSTEG.md`, `docs/BESLUT.md`, `docs/UPPGIFTER.md`.
- Bygg i små steg, kör `npm run build` efter varje ändring, fråga vid större vägval.
