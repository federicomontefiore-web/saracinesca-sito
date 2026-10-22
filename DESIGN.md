# DESIGN.md — Saracinesca (nome provvisorio)

Direzione: **caldo e artigianale, con un filo tecnico.** La bottega sotto casa che ti sistema tutto: carta, inchiostro, un rosso mattone romano. Il motivo grafico è la **saracinesca** (righe orizzontali a lamelle), usato con parsimonia: hero e divisori, mai come sfondo ovunque.
Solo modalità chiara (per ora).

## Colore

| Token | Valore | Ruolo |
|---|---|---|
| `--paper` | #F6F1E7 | sfondo pagina |
| `--paper-2` | #EDE5D6 | sezioni alternate, fasce |
| `--surface` | #FFFDF8 | card prezzi, riquadri |
| `--ink` | #1F1B16 | testo principale, titoli |
| `--ink-2` | #5A5148 | testo secondario (7.0:1 su paper) |
| `--line` | #D8CDBA | bordi, divisori |
| `--brick` | #A63D1A | primario: bottoni, link, evidenze (6.1:1 con bianco) |
| `--brick-dark` | #84300F | hover/pressed del primario |
| `--ochre` | #D9A441 | accento decorativo (lamelle, sottolineature). Mai per testo. |
| `--steel` | #3B4148 | saracinesca, sezione scura finale |
| `--ok` | #2F6B4F | conferme |
| `--err` | #B3261E | errori |

## Tipografia

- Titoli: **Fraunces** (serif con carattere, pesi 600/700, opsz automatico).
- Testo: **IBM Plex Sans** (400/500/600) — il lato "tecnico".
- Scala (px / line-height): 14/1.5 · 16/1.6 (body) · 18/1.6 (lead) · 22/1.35 · 28/1.25 · 36/1.15 · 48/1.05 · 64/1.0 (h1 desktop).
- Righe di testo max 65ch.

## Spazi

Scala 8: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128. Sezioni: 96px desktop / 64px mobile. Contenuto max 1160px, gutter 20px mobile.

## Forma e profondità

Raggi: 4px (input, tag), 10px (card, bottoni). Un'ombra sola: `0 1px 0 var(--line), 0 12px 32px -16px rgba(31,27,22,.25)` per la card evidenziata. Il resto è piatto, con bordi.

## Componenti

- **Bottone primario**: brick, testo bianco, 48px alto, hover brick-dark, focus anello ochre 3px + offset.
- **Bottone secondario**: bordo ink 1.5px, sfondo trasparente.
- **Link**: brick, sottolineato, spessore 1.5px.
- **Card pacchetto**: surface, bordo line; quella consigliata con bordo brick 2px e ombra.
- **Segnaposto**: riquadro tratteggiato ochre con etichetta "DA INSERIRE".
- Nav sticky su paper, collassa in menu su mobile.

## Immagini e icone

Icone a tratto 1.75px, disegnate inline in SVG, stile semplice. Niente emoji, niente foto stock: foto vere dei lavori quando arrivano, altrimenti segnaposto dichiarati.
