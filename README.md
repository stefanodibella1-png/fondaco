# Fondaco

Rete di B&B, case vacanza e affittacamere siciliani. *Arrivi ospite, riparti di casa.*

Online: **https://fondaco-sicilia.netlify.app**

Prototipo statico, nessuna build necessaria.

| Percorso | Cosa contiene |
|---|---|
| `/` | Sito vetrina in 3D: volo sull'isola, passeggiata nel borgo, viaggio in carretto. Dati di esempio (3.490 strutture). |
| `/control-center/` | Control center dell'host: personalizza l'app della struttura con anteprima dal vivo e maiolica con QR. |
| `/logo/` | Quattro proposte di logo. |

## Pubblicazione su Netlify

Netlify → **Add new site → Import an existing project → GitHub** → scegli questo repository.
Build command vuoto, publish directory `.` (già impostati in `netlify.toml`). Ogni push su `main` ripubblica il sito.

## Librerie esterne

- three.js r128 (cdnjs) e i suoi esempi (OrbitControls, bloom) da jsDelivr
- qrcodejs 1.0.0 (cdnjs) nel control center
- Font: Abril Fatface, Albert Sans, JetBrains Mono (Google Fonts)

## Prossimi passi

Versione di produzione: Next.js (App Router) + TypeScript + Tailwind su Vercel, Supabase (Postgres, Auth magic link, Storage, RLS su tutte le tabelle), Stripe per l'abbonamento annuale, italiano e inglese.
La configurazione di ogni struttura (vedi *Configurazione* nel control center) diventa una riga su Supabase.
