# MARIO Android — Handoff B34.10

## Stato
Build verde ✅ — APK debug + AAB release disponibili via GitHub Actions

## Dati app
| Campo | Valore |
|---|---|
| Package | `com.homemario.app` |
| URL | `https://app.homemario.com` |
| minSdk | 21 (Android 5.0+) |
| targetSdk | 35 |
| compileSdk | 36 |
| Versione | 1.0.0 (versionCode 1) |

## Keystore (LOCALE — non in git)
| Campo | Valore |
|---|---|
| File | `android.keystore` |
| Alias | `android` |
| Password store | `homemario2024` |
| Password key | `homemario2024` |
| SHA256 | `A5:AC:FB:52:54:1F:5D:7A:94:D7:27:E0:07:C7:85:DA:CF:7D:42:4D:92:89:98:70:BF:97:BF:BF:76:12:F6:99` |
| Validità | fino al 2053 |

**BACKUP KEYSTORE OBBLIGATORIO** — senza di esso non si può aggiornare l'app sul Play Store.

## Digital Asset Links
`https://app.homemario.com/.well-known/assetlinks.json` ✅ live

## GitHub Actions
- **Debug APK**: build automatico su ogni push → artefatto `mario-debug-apk`
- **Release AAB**: build automatico → artefatto `mario-release-aab`
- Secrets configurati: `KEYSTORE_BASE64`, `KEY_ALIAS`, `KEY_STORE_PASSWORD`, `KEY_PASSWORD`

## Prossimo passo manuale — Play Store

1. **Crea account Google Play Developer** (25 USD una tantum) su `play.google.com/console`
2. **Crea nuova app** → inserisci package `com.homemario.app`
3. **Scarica AAB** dagli artefatti GitHub Actions (Run verde → mario-release-aab)
4. **Carica AAB** in Play Console → Test interno → poi Produzione
5. **Compila scheda store**: nome "MARIO", descrizione, screenshot, icona (store_icon.png già presente)
6. **Content rating**: compila questionario
7. **Submit per review** (1-3 giorni)

## Commit storia B34.10
| Commit | Descrizione |
|---|---|
| `684730a` | Init TWA |
| `cd5dd6e` | Fix compileSdk 36 — build verde |
| ultimo | Workflow release AAB + handoff |
