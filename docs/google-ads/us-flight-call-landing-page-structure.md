# Structure LP — vols US réservés par téléphone (mobile-first)

Document **front-ready** : chaque section indique **objectif**, **contenu**, **copy proposé** (EN, factuel), **risques / validation** avant mise en ligne.  
**Ne pas publier** sans validation **acheteur Marketcall + juridique** (entité légale, numéro, claims oraux, preuves).

---

## 0. Meta & head (non visible mais bloquant)

| Élément | Rôle | Notes |
|--------|------|--------|
| `<title>` | SERP / onglet | 50–60 car. max ; aligné H1 sans spam. |
| `meta description` | Snippet | Factuel ; pas de prix garanti. |
| `canonical` | URL finale HTTPS | = URL Google Ads final. |
| `viewport` + `theme-color` | Mobile | `viewport-fit=cover` si barre sticky basse. |
| `robots` | Indexation | `index,follow` sauf consigne contraire. |
| Open Graph | Partage | Titre + description alignés LP. |
| JSON-LD `WebPage` / `FAQPage` | Rich results | Dupliquer **exactement** le texte visible FAQ si FAQPage utilisé. |

**Copy proposé (title / description)** — à adapter au nom commercial réel :

- **Title** : `Book U.S. domestic flights by phone | [Brand]`  
- **Description** : `Call to compare options for U.S. domestic flights. We are not the airline. Total price before you pay. Operated by [Legal entity].`

---

## 1. Hero (above the fold)

| Champ | Détail |
|--------|--------|
| **Objectif** | Clarifier offre + CTA appel en < 5 s ; réduire rebond. |
| **Contenu** | H1 court ; 1–2 lignes de support ; **pas** de faux compteur ; numéro ou bouton `tel:` visible. |
| **Disclaimer** | Ligne fine ou badge : *Independent booking help — not Delta, United, or American Airlines.* |
| **CTA primaire** | Bouton large « Call now » + `tel:` (même numéro que Google forwarding). |
| **Risque** | H1 trop prometteur (« cheapest ») → policy. |

**Copy proposé (EN)** — synchroniser avec tests AB (`us-flight-call-hero-ab-variants.md`) :

- **H1 (slot)** : voir variante A/B retenue pour la v1.  
- **Sous-texte** : `Live agents for U.S. domestic flights. Fees and total price explained before you pay.`  
- **Micro-trust** : `Operated by [Legal entity].`

---

## 2. Bloc « Not affiliated / not the airline » (callout dédié)

| Champ | Détail |
|--------|--------|
| **Objectif** | Éviter confusion marque ; alignement annonces d’appel + extensions. |
| **Contenu** | Encadré court ; pas de petits caractères illisibles ; contraste AA. |
| **Risque** | Absence = suspicion / refus acheteur. |

**Copy proposé (EN)** :

> **We are not the airline.** We help you book **U.S. domestic** flights by phone. Flights are operated by the airline shown on your ticket.

---

## 3. How it works (3–4 étapes)

| Champ | Détail |
|--------|--------|
| **Objectif** | Réduire peur arnaque ; expliquer IVR si applicable. |
| **Contenu** | Numéroté 1–4 ; verbes d’action ; pas de SLA chiffré sans preuve. |

**Copy proposé (EN)** (exemple générique) :

1. `Tap Call and reach our queue.`  
2. `If prompted, follow the short IVR to confirm you want U.S. domestic flight booking help.`  
3. `Tell the agent your dates and cities; hear total price before you pay.`  
4. `Pay only if you choose to complete a booking.`

*(Si l’offre n’a pas d’IVR, retirer l’étape 2.)*

---

## 4. Proof / trust (factuel uniquement)

| Champ | Détail |
|--------|--------|
| **Objectif** | Crédibilité sans témoignages inventés. |
| **Contenu** | Entité légale + état d’enregistrement si autorisé ; pas de logos compagnies suggérant partenariat officiel. |
| **Risque** | Logos « Delta / United / American » sans disclaimer → trademarks / misrepresentation. |

**Copy proposé (EN)** :

- `Operated by [Legal entity], [State/country].`  
- `We do not represent any airline brand as an official site.`

---

## 5. FAQ (module)

| Champ | Détail |
|--------|--------|
| **Objectif** | Répondre aux frictions (prix, paiement, qui vous êtes, privacy). |
| **Contenu** | Réutiliser / coller depuis `docs/google-ads/us-flight-call-landing-faq.md` (version EN LP) ; garder parité visible ↔ JSON-LD. |

---

## 6. Fees & transparency (court bloc)

| Champ | Détail |
|--------|--------|
| **Objectif** | Honnêteté prix / politique trompeuse. |
| **Contenu** | Pas de « guaranteed lowest » ; « total price before you pay ». |

**Copy proposé (EN)** :

> Airfare changes with dates and availability. The agent states your **total** price (fare and applicable taxes/fees) **before** you authorize payment.

---

## 7. Privacy / CCPA (lien + une ligne)

| Champ | Détail |
|--------|--------|
| **Objectif** | Confiance + obligations US. |
| **Contenu** | Lien `Privacy policy` ; phrase CCPA si Californie ciblée. |

**Copy proposé (EN)** :

> We use your information to handle this call and booking request. See our Privacy Policy. California residents: see our CCPA notice (if applicable).

---

## 8. CTA sticky (bas d’écran, mobile)

| Champ | Détail |
|--------|--------|
| **Objectif** | Conversion appel sans scroll back. |
| **Contenu** | Barre fixe : libellé court + `tel:` ; `padding-bottom` safe-area ; ne pas masquer contenu critique (scroll padding sur `body`). |
| **Risque** | CTA différent du numéro annonce → désalignement tracking. |

**Comportement** : même numéro et même libellé que hero CTA.  
**Wireframe ASCII (sticky)** :

```
┌──────────────────────────────────────┐
│  [  Call now  ]  +1 (___) ___-____   │
└──────────────────────────────────────┘
```

---

## 9. Footer légal

| Champ | Détail |
|--------|--------|
| **Objectif** | Mentions obligatoires brief ; copyright ; liens légaux. |
| **Contenu** | © [Year] [Brand] · Privacy · Terms · (Do Not Sell si requis). |

---

## 10. Ordre de scroll recommandé (mobile)

1. Hero + CTA  
2. Not affiliated callout  
3. How it works  
4. Fees & transparency  
5. Proof  
6. FAQ  
7. Privacy line  
8. Footer  
9. *(Sticky CTA superposé en permanence — z-index au-dessus du footer mais sans cacher liens légaux : footer avec marge basse suffisante.)*

---

## 11. Checklist builder (binaire)

- [ ] Un seul numéro `tel:` partout = numéro Google / Marketcall validé.  
- [ ] H1 + sous-texte + callout = **cohérents** avec RSA / extensions.  
- [ ] Aucune promesse de prix / délai non vérifiable au téléphone.  
- [ ] FAQ visible = FAQ JSON-LD si FAQPage présent.  
- [ ] Sticky CTA testé iOS Safari + Android Chrome (safe area).
