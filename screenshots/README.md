---
layout: default
title: Screenshots
---


# Blocktomic — Screenshots

## Cartelle

```
screenshots/
├── play_store/          # 8 screenshot per Google Play Store (1920×1080 px min)
│   ├── 01_workout_library.png
│   ├── 02_workout_editor.png
│   ├── 03_timer_running.png
│   ├── 04_gps_tracking.png
│   ├── 05_progress_badges.png
│   ├── 06_settings_personalization.png
│   ├── 07_support_screen.png
│   └── 08_completed_workout.png
├── guide/               # Screenshot per la guida utente
│   ├── workout_library.png
│   ├── workout_editor.png
│   ├── workout_preview.png
│   ├── timer_running.png
│   ├── gps_tracking.png
│   ├── progress_badges.png
│   ├── settings_personalization.png
│   ├── history_detail.png
│   ├── profile_screen.png
│   ├── feedback_overlay.png
│   ├── language_settings.png
│   ├── onboarding_privacy.png
│   └── README.md
└── README.md
```

## Screenshot disponibili

La cartella `guide/` contiene tutti gli screenshot referenziati dalle guide:

| File | Contenuto | Usato in |
|---|---|---|
| `onboarding_welcome.jpeg` | Pagina di benvenuto dell'onboarding | USER_GUIDE §1 |
| `onboarding_preferences.jpeg` | Pagina preferenze (unità + famiglie) | USER_GUIDE §1 |
| `onboarding_suggestions.jpeg` | Pagina suggerimenti con selettore stile nomi | USER_GUIDE §1 |
| `home_screen.jpg` | Home con obiettivo, focus e card workout | USER_GUIDE §2 |
| `library_filters.png` | Libreria con 2 tab (Recent/Workouts) e pannello filtri | USER_GUIDE §4 |
| `workout_card_anatomy.png` | Card libreria con titolo spiritoso, nome classico e riga info | USER_GUIDE §4, FEATURES_GUIDE |
| `progress_muscles.png` | Progress con serie, badge e distribuzione muscoli | USER_GUIDE §9 |
| `share_qr_sheet.png` | Bottom sheet di condivisione con codice QR | USER_GUIDE §8, FEATURES_GUIDE |
| `settings_appearance.png` | Impostazioni – aspetto (accent, stili, nomi divertenti) | USER_GUIDE §11, FEATURES_GUIDE |
| `language_settings.png` | Impostazioni – lingua e aspetto | USER_GUIDE §11 |
| `feedback_ideas.png` | Feedback & Ideas con votazioni feature | FEATURES_GUIDE |
| `timer_running.png` | Timer a schermo intero durante un blocco | WORKOUT_GUIDE |
| `gps_tracking.png` | Tracciamento GPS con barra di progresso e velocità | WORKOUT_GUIDE |
| `workout_editor.png` | Editor workout con blocchi | WORKOUT_GUIDE |
| `trend_charts.png` | Schermata Trend con selettore metrica | USER_GUIDE §9 |
| `history_week.png` | Cronologia settimanale | USER_GUIDE §9 |

La cartella `play_store/` contiene le 8 immagini per la scheda Google Play Store
(le versioni `.v1.png` e `.v2.png` sono scarti precedenti e possono essere ignorate).

Altri screenshot presenti ma non referenziati nei documenti: `feedback_overlay.png`,
`profile_screen.png`, `workout_preview.png`, `history_detail.png`, `onboarding_privacy.png`.

---

## Come rigenerare gli screenshot (UI v1.0.2+)

> ⚠️ **Nota**: gli screenshot attuali riflettono una versione precedente dell'interfaccia.
> Dopo le modifiche alla UI (Home con obiettivi/focus, libreria con 2 tab e pannello
> filtri, sezione muscoli in Progress), vanno **rigenerati**.

### Prerequisiti
1. Telefono Android con **debugging USB** abilitato, collegato via USB (o ADB over WiFi).
2. App installata e in **lingua INGLESE** (`Settings > Language > English`).
3. ADB (lo script lo installa da solo se manca).

### Esecuzione
```bash
./scripts/take_screenshots.sh
```

Lo script è **semi-manuale**: per ogni screenshot vi ferma e vi chiede di aprire la
schermata sul telefono, poi premete ENTER per catturarla. Salva direttamente in
`blocktomic-docs/screenshots/`. Di seguito la sequenza esatta di navigazione.

### Play Store (8) — per Google Play
| # | File (in `play_store/`) | Schermata da aprire sul telefono |
|---|---|---|
| 1 | `01_workout_library.png` | **Home**: obiettivo e focus in alto, card workout sotto |
| 2 | `02_workout_editor.png` | Un workout → **Create/Edit** |
| 3 | `03_timer_running.png` | **Timer** in esecuzione (es. Classic Tabata) |
| 4 | `04_gps_tracking.png` | **GPS** durante un interval a distanza |
| 5 | `05_progress_badges.png` | **Progress** con badge + distribuzione muscoli |
| 6 | `06_settings_personalization.png` | **Impostazioni** > stile/colore e obiettivi/focus |
| 7 | `07_support_screen.png` | Schermata **Support** |
| 8 | `08_completed_workout.png` | Workout **completato** o cronologia |

### Guida utente (16) — per le guide
| # | File (in `guide/`) | Schermata da aprire sul telefono |
|---|---|---|
| G1 | `onboarding_welcome.jpeg` | Benvenuto (fresh install / reimposta) |
| G2 | `onboarding_preferences.jpeg` | Onboarding > Preferenze (unità + famiglie) |
| G3 | `onboarding_suggestions.jpeg` | Onboarding > Suggerimenti (stile nomi) |
| G4 | `home_screen.jpg` | **Home** (obiettivo + focus + card) |
| G5 | `library_filters.png` | **Libreria** (2 tab + pannello filtri aperto) |
| G6 | `workout_card_anatomy.png` | Libreria > una card workout |
| G7 | `progress_muscles.png` | **Progress** con muscoli |
| G8 | `trend_charts.png` | Trend con selettore metrica |
| G9 | `history_week.png` | Cronologia settimanale |
| G10 | `settings_appearance.png` | Impostazioni > aspetto |
| G11 | `language_settings.png` | Impostazioni > Lingua (elenco) |
| G12 | `share_qr_sheet.png` | Condivisione (bottom sheet QR) |
| G13 | `timer_running.png` | Timer a schermo intero |
| G14 | `gps_tracking.png` | GPS con barra di progresso e velocità |
| G15 | `workout_editor.png` | Editor con blocchi |
| G16 | `feedback_ideas.png` | Feedback & Ideas con votazioni |

### Dopo la cattura
1. Verificate dimensioni ≥ 1920×1080 per i file `play_store/` (croppate se serve).
2. Allineate i link nelle guide a eventuali file rinominati.
3. Caricate gli 8 screenshot su **Play Console**, abbinandoli alle didascalie in
   `docs/STORE_TEXT_8_LANG.md` (§ Screenshot Captions).