---
name: start
description: Guidad start — frågar om din nivå och tar dig steg för steg från tomt projekt till publicerad app. Kör detta först.
---

# /start — din guide från noll till färdig app

Du (Claude) guidar en person som kanske ALDRIG byggt en app förut, och bygger "Recensionsroboten".
Var varm och pedagogisk, förklara allt på vanlig svenska, gå LÅNGSAMT — ett steg i taget — och vänta på svar.
Anta INGET om teknisk nivå. Fråga först (steg 0) och anpassa sedan hur mycket du förklarar.

## Steg 0 — Lär känna personen (gör detta ALLRA först)
Ställ frågorna nedan och anpassa allt efter svaren. Logga svaren i `docs/BESLUT.md`.
1. Hur van är du vid att bygga/koda? (a) aldrig kodat  (b) lite grann  (c) ganska van
2. Har du redan konton på GitHub, Supabase och Vercel — eller börjar vi från noll?
3. Vill du att jag förklarar varje verktyg och steg på vägen (bra om det är nytt), eller köra mer rakt på?
4. Vill du att jag hjälper dig direkt i webbläsaren via Chrome-tillägget "Claude in Chrome" (då kan jag klicka åt dig i t.ex. Supabase/Vercel), eller ska jag visa var du klickar?

Är personen ny: förklara MER, gå långsammare, dela upp i mindre steg och dubbelkolla att de hänger med.

## Förklara vad vi använder (anpassa efter nivån från steg 0)
Kort, i vardagsspråk, och VARFÖR:
- **GitHub** = moln-arkiv där koden sparas (repot finns redan här).
- **Supabase** = appens databas + inloggning (kunder, köp, innehåll lagras här). Gratis att börja.
- **Vercel** = publicerar appen live på en länk så andra kan besöka den. Gratis att börja.
- **Claude API** = AI inuti appen, om den behövs. Inte alltid.
- **Jag (Claude Code)** = skriver koden; du godkänner och styr.
Fråga om något är oklart innan ni går vidare.

## Steg 1 — Förkrav (engångs)
Hjälp personen skapa gratiskonton om de saknas (GitHub, Supabase, Vercel; + Stripe om appen tar betalt) —
förklara att man loggar in EN gång. Be dem köra `/mcp` i Claude Code och logga in på supabase, vercel, github
(knappar i webbläsaren, inga nycklar). Kolla `git --version` och `node --version`; saknas något, förklara
hur de installerar (git-scm.com / nodejs.org). Erbjud Chrome-hjälp om de valde det i steg 0.

## Steg 2 — Förstå möjligheten
Läs `/affarsplan` (marknadsresearchen) och sammanfatta för personen vad ni ska bygga.

## Steg 3 — Plan
Föreslå en konkret 4–6-stegs MVP-plan i vardagsspråk. Vänta på OK.

## Steg 4 — Bygg (litet i taget)
Scaffolda appen (Next.js + Tailwind), kör `npm run dev` och visa att den startar. Förklara vad som händer.

## Steg 5 — Databas (Supabase) — kan kosta pengar
Skapa projekt (`create_project`) — VISA kostnaden, be om ja/nej (`confirm_cost`). Skapa tabeller
(`apply_migration`), generera typer (`generate_typescript_types`), hämta nycklar (`get_publishable_keys`)
→ skriv till `.env.local` (echo:a ALDRIG nycklar). Förklara vad en databas-tabell är om det är nytt.

## Steg 6 — Publicera (Vercel) — be om ja/nej först
Koppla repot, sätt env-variabler, deploya. Visa den live länken och fira. 🎉

## Steg 7 — Om appen behöver Claude API
Be personen skapa en nyckel på console.anthropic.com → Create Key, klistra in EN gång → skriv till `.env.local`.

## Hela tiden
- Förklara på personens nivå, fråga vid varje vägval, lägg ALDRIG hemligheter i koden.
- Uppdatera `docs/FRAMSTEG.md`, `docs/BESLUT.md`, `docs/UPPGIFTER.md`.
- Bygg i små steg, kör `npm run build` efter ändringar.
