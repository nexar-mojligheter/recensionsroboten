# Recensionsroboten

> Researchad affärsmöjlighet från Nexar Academy. Den fullständiga marknadsresearchen
> ligger i skillen **affärsplan** — kör `/affarsplan` för att läsa den.

## Vad vi bygger
AI-svar på Google-recensioner – skräddarsytt för svenska restauranger och deras SEO-ranking 2026.. Recensionsroboten svarar automatiskt på dina Google-recensioner med en ton och stil som passar just restaurangbranschen – inte ett generiskt svar som lika gärna kunde komma från en bilverkstad. Varje svar är optimerat för att stärka din synlighet i Google, Gemini och ChatGPT, som 2026 rankar restauranger direkt efter hur aktivt de hanterar recensioner. Spara timmar varje vecka och sluta aldrig synas i AI-drivna sökresultat.

## Stack (ändra inte utan att fråga)
- Next.js + Tailwind (frontend)
- Supabase (databas + auth)
- Vercel (deploy)
- Claude API där appen behöver AI

## Kommandon
- `npm run dev` — kör lokalt
- `npm run build` — bygg + felkoll (kör efter varje ändring)
- `npm run lint` — lint

## Så jobbar vi (viktigt)
- Bygg i **små steg** — kör `npm run build` efter varje ändring och visa resultatet.
- **Fråga vid större vägval** (tech, datamodell, pris) i stället för att gissa.
- Lägg **aldrig** hemligheter/nycklar i koden — bara i `.env.local`.
- Håll det **enkelt** — en MVP som bevisar värdet, inte en färdig produkt.

## Projektminne (DU ansvarar för det — användaren ska aldrig behöva be)
- Efter varje avklarat steg: uppdatera `docs/FRAMSTEG.md` (byggt + nästa steg).
- Vid varje vägval: logga en rad i `docs/BESLUT.md` (datum + 1 mening om varför).
- Bocka av i `docs/UPPGIFTER.md` allt eftersom.
- **Vid sessionsstart: läs `docs/FRAMSTEG.md` FÖRST** och sammanfatta "var vi var".
- Använd din inbyggda auto-memory för build-kommandon och buggfixar.

## Kom igång
Läs `/affarsplan`, föreslå sedan en konkret **4–6-stegsplan** för MVP:n — sen kör vi.

<!-- nexar:opportunity slug=recensionsroboten -->
