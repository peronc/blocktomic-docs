---
layout: default
title: Screenshots
---


# Blocktomic — Screenshots

## Cartelle

```
screenshots/
├── play_store/                 # 8 PNG 1080×1920 per Google Play Store
│   ├── 01_workout_library.png
│   ├── 02_workout_editor.png
│   ├── 03_timer_running.png
│   ├── 04_gps_tracking.png
│   ├── 05_progress_badges.png
│   ├── 06_settings_personalization.png
│   ├── 07_workout_preview_muscles.png
│   ├── 08_completed_workout.png
│   ├── raw/                    # catture native 1080×2400 (input dello script)
│   └── archive/                # scarti delle versioni precedenti
└── guide/                      # screenshot per la guida utente
    ├── onboarding_welcome.jpeg
    ├── onboarding_preferences.jpeg
    ├── onboarding_suggestions.jpeg
    ├── home_screen.jpg
    ├── library_filters.png
    ├── workout_card_anatomy.png
    ├── progress_muscles.png
    ├── trend_charts.png
    ├── history_week.png
    ├── settings_appearance.png
    ├── language_settings.png
    ├── share_qr_sheet.png
    ├── timer_running.png
    ├── gps_tracking.png
    ├── workout_editor.png
    ├── feedback_ideas.png
    └── archive/                # scarti non referenziati
```

## Screenshot disponibili

La cartella `guide/` contiene tutti gli screenshot referenziati dalle guide:

| File | Contenuto | Usato in |
|---|---|---|
| `onboarding_welcome.jpeg` | Pagina di benvenuto (titolo + accent color) | USER_GUIDE §1 |
| `onboarding_preferences.jpeg` | Preferenze (categoria, unità, reminder) | USER_GUIDE §1 |
| `onboarding_suggestions.jpeg` | Suggerimenti con selettore stile nomi | USER_GUIDE §1 |
| `home_screen.jpg` | Home con obiettivo, focus e card workout | USER_GUIDE §2 |
| `library_filters.png` | Libreria con tab e pannello filtri | USER_GUIDE §4 |
| `workout_card_anatomy.png` | Card libreria con titolo, nome classico e riga info | USER_GUIDE §4, FEATURES_GUIDE |
| `progress_muscles.png` | Progress con serie, badge e distribuzione muscoli | USER_GUIDE §9 |
| `trend_charts.png` | Trend con selettore metrica e distribuzione muscoli | USER_GUIDE §9 |
| `history_week.png` | Cronologia settimanale (heatmap) | USER_GUIDE §9 |
| `share_qr_sheet.png` | Bottom sheet di condivisione con codice QR | USER_GUIDE §8, FEATURES_GUIDE |
| `settings_appearance.png` | Impostazioni – aspetto (accent, stili) | USER_GUIDE §11, FEATURES_GUIDE |
| `language_settings.png` | Impostazioni – lingua (elenco) | USER_GUIDE §11 |
| `feedback_ideas.png` | Feedback & Ideas con votazioni feature | FEATURES_GUIDE |
| `timer_running.png` | Timer a schermo intero (timeline + Rate) | WORKOUT_GUIDE |
| `gps_tracking.png` | Tracciamento GPS con barra di progresso e velocità | WORKOUT_GUIDE |
| `workout_editor.png` | Editor workout con blocchi | WORKOUT_GUIDE |

La cartella `play_store/` contiene le 8 immagini per la scheda Google Play Store.
Sono **PNG 1080×1920 (9:16) senza alpha**, conformi ai requisiti Google Play
(lato 320–3840 px, rapporto max 2:1, idonei alla promozione a 1080 px).

---

## Come rigenerare gli screenshot (UI v1.0.4+)

Gli screenshot riflettono la UI v1.0.4 (pulsante Rate, etichette "Set X of Y",
sezione muscoli nell'anteprima, timeline interattiva). Per rigenerarli:

### Prerequisiti
1. Telefono Android con **debugging USB** abilitato, collegato via USB (o ADB over WiFi).
2. App installata e in **lingua INGLESE** (`Settings > Language > English`).
3. ADB (lo script lo installa da solo se manca).

### Cattura
```bash
./scripts/take_screenshots.sh
```
Lo script è **semi-manuale**: per ogni screenshot vi ferma e vi chiede di aprire la
schermata sul telefono, poi premete ENTER. Le catture Play Store finiscono in
`play_store/raw/` (native 1080×2400); quelle della guida direttamente in `guide/`.

> Per le pagine di onboarding (`onboarding_*`) serve uno stato pulito: eseguite
> `adb shell pm clear com.ramyralabs.blocktomic` e riaprite l'app. Al primo avvio
> compare il popup di consenso "Share anonymous usage data" e quello di sistema per
> le notifiche: chiudeteli prima di catturare la pagina di benvenuto.

### Play Store (8) — per Google Play
| # | File (in `play_store/raw/`) | Schermata da aprire sul telefono |
|---|---|---|
| 1 | `01_workout_library.png` | **Home**: obiettivo e focus in alto, card workout sotto |
| 2 | `02_workout_editor.png` | Un workout → **Create/Edit** |
| 3 | `03_timer_running.png` | **Timer** in esecuzione con timeline e pulsante **Rate** |
| 4 | `04_gps_tracking.png` | **GPS** durante un interval a distanza |
| 5 | `05_progress_badges.png` | **Progress** con badge + distribuzione muscoli |
| 6 | `06_settings_personalization.png` | **Impostazioni** > accent e stile |
| 7 | `07_workout_preview_muscles.png` | **Anteprima workout** con sezione muscoli |
| 8 | `08_completed_workout.png` | **Feedback** di fine serie (peso, reps, valutazione) |

### Guida utente (16) — per le guide
| # | File (in `guide/`) | Schermata da aprire sul telefono |
|---|---|---|
| G1 | `onboarding_welcome.jpeg` | Benvenuto (fresh install / clear data) |
| G2 | `onboarding_preferences.jpeg` | Onboarding > Preferenze (categorie + unità) |
| G3 | `onboarding_suggestions.jpeg` | Onboarding > Suggerimenti (stile nomi) |
| G4 | `home_screen.jpg` | **Home** (obiettivo + focus + card) |
| G5 | `library_filters.png` | **Workouts** con pannello filtri aperto |
| G6 | `workout_card_anatomy.png` | Workouts > una card workout |
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

### Post-processing (solo Play Store)
Le catture native 1080×2400 non sono valide per Play (rapporto 2,22:1 > 2:1).
Lo script le converte in PNG 1080×1920 con sfondo brand, angoli arrotondati e
rimozione dell'alpha:
```bash
python3 scripts/process_store_screenshots.py
```
Output: `play_store/01…08.png` (verificate dimensioni, assenza di alpha e peso ≤ 8 MB).

### Dopo la cattura
1. Allineate le didascalie in `docs/PLAY_STORE_LISTING.md` e `docs/STORE_TEXT_8_LANG.md`.
2. Caricate gli 8 PNG su **Play Console**, abbinandoli alle caption per lingua.
