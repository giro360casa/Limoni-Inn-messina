# Hotel Cairoli – Tour Virtuale 360°
> Powered by [Giro360](https://giro360.casa)

## 📁 Struttura del progetto

```
hotel-cairoli-tour/
└── index.html   ← tutto il necessario in un solo file
```

---

## ⚙️ Configurazione

Apri `index.html` e modifica il blocco **TOUR_CONFIG** (circa riga 190):

```js
const TOUR_CONFIG = {

  // ── OPZIONE A: immagine 360° equirettangolare ──────────
  imageUrl: "https://tuosito.com/foto360.jpg",  // ← URL della tua foto
  useIframe: false,

  // ── OPZIONE B: embed esterno (Matterport, Kuula, ecc.) ─
  useIframe: true,
  iframeSrc: "https://kuula.co/share/TOUR_ID?fs=1&vr=0",

  // ── Pannellum ──────────────────────────────────────────
  title:      "Hotel Cairoli",
  author:     "Giro360",
  autoRotate: -2,   // gradi/secondo (0 = disattivato)
};
```

Aggiorna anche i link social nella card (Instagram, WhatsApp, Email, Sito Web).

---

## 🚀 Deploy su GitHub + Vercel (5 minuti)

### 1. Crea repository su GitHub

```bash
git init
git add index.html
git commit -m "feat: tour virtuale Hotel Cairoli"
git remote add origin https://github.com/TUO_USERNAME/hotel-cairoli-tour.git
git push -u origin main
```

### 2. Collega Vercel

1. Vai su [vercel.com](https://vercel.com) e accedi con GitHub
2. Clicca **Add New → Project**
3. Seleziona il repository `hotel-cairoli-tour`
4. Framework Preset → **Other** (nessun framework, solo HTML statico)
5. Clicca **Deploy**

Vercel pubblica automaticamente su un URL del tipo:
```
https://hotel-cairoli-tour.vercel.app
```

### 3. Dominio personalizzato (opzionale)

In Vercel → Settings → Domains, aggiungi:
```
tour.hotelcairoli.it
```
e configura il record CNAME sul tuo DNS.

---

## 📸 Come aggiungere la tua foto 360°

| Formato | Consigliato |
|---------|------------|
| Tipo    | Equirettangolare (2:1) |
| Risoluzione | min 4000×2000px, ideale 8000×4000px |
| Formato | JPEG (.jpg) |
| Hosting | Carica su Cloudinary, Vercel `/public`, o qualsiasi CDN |

---

## 🔗 Integrazioni esterne supportate

| Servizio     | Come usarlo |
|-------------|-------------|
| **Kuula**   | `useIframe: true` + URL share Kuula |
| **Matterport** | `useIframe: true` + URL embed Matterport |
| **Giro360** | `useIframe: true` + URL del tour Giro360 |
| **Pannellum** | `useIframe: false` + URL immagine 360° |

---

## ✏️ Personalizzazioni rapide

| Cosa cambiare | Dove |
|--------------|------|
| Nome hotel, testo benvenuto | Sezione `.card` nell'HTML |
| Colore oro `#c9a84c` | Variabile `--gold` nel CSS |
| Immagine di sfondo | URL in `#bg { background }` |
| Link social/contatti | Sezione `.socials` e `.contacts` |

---

*Realizzato da [Giro360](https://giro360.casa) – Tour virtuali 360° per strutture ricettive e agenzie immobiliari.*
