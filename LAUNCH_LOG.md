# Launch Log — Speak with Claw

**Datum:** 23.02.2026
**Status:** App Store Review ausstehend

---

## Was wurde gemacht

### GitHub
- Repo public: https://github.com/JHAppsandBots/speak-with-openclaw-ios
- Release v1.0 erstellt
- App Icon (Krabbe mit Telefon) aus `Logo_Claw_phone.png` generiert (alle Größen)
- Topics gesetzt: ios, swift, telegram, voice-assistant, self-hosted, openclaw, vad, iphone
- Homepage: https://openclaw.ai
- CHANGELOG.md erstellt
- SETUP.md (End-User Anleitung) erstellt
- PRIVACY_POLICY.md erstellt
- GitHub Pages aktiviert → Privacy Policy URL: https://jhappsandbots.github.io/speak-with-openclaw-ios/privacy
- Hardcoded Tailscale-IP ersetzt durch `YOUR_MAC_IP` Placeholder
- Early Release Disclaimer in README

### App Store Connect
- App ID: `6759576522`
- Bundle ID: `de.johanneshahn.speakwithopenclaw`
- Build hochgeladen via `xcrun altool` (IPA aus separatem Public-Projekt)
- Metadata hochgeladen (Name, Subtitle, Beschreibung, Keywords, URLs)
- 3 Screenshots manuell hochgeladen (1290x2796, iPhone 6.7")
- Preis: Kostenlos
- Verfügbarkeit: Alle Länder
- Copyright: © 2026 Johannes Hahn
- Datenschutz-URL: https://jhappsandbots.github.io/speak-with-openclaw-ios/privacy
- Support-URL: https://github.com/JHAppsandBots/speak-with-openclaw-ios
- Zur Review eingereicht: 23.02.2026 ~22:40

### Reddit
- Post-Text fertig (für r/selfhosted + r/iosprogramming)
- Moderatoren angeschrieben (warten auf Antwort)
- Falls keine Antwort nach 2 Tagen: einfach posten

---

## Credentials & Keys

- **Apple Developer Account:** johanneshey-music.com
- **Team ID:** 9YMCY74WN3
- **Auth Key ID:** MF465S89A3
- **Key Path:** `~/.appstoreconnect/private_keys/AuthKey_MF465S89A3.p8`
- **Issuer ID:** 6b3c7a6c-b1e8-41f7-b879-1f69545dbd36
- **App Store Connect App ID:** 6759576522

→ Vollständige Credentials: `../.claude/credentials/CREDENTIALS.md`

---

## Fastlane Setup

```bash
cd SpeakWithOpenClaw-Public

# Nur Metadata hochladen
fastlane upload_metadata

# Nur Screenshots hochladen
fastlane upload_screenshots
```

---

## Nächste Schritte

- [ ] Apple Review abwarten (1-2 Tage)
- [ ] Reddit-Post abfeuern (nach Mod-Antwort oder nach 2 Tagen)
- [ ] GitHub Traffic beobachten: Repo → Insights → Traffic
- [ ] Bei neuem Build: `xcodegen generate` + `xcodebuild archive` + `xcrun altool --upload-app`

---

## Projekt-Struktur

```
SpeakWithOpenClaw-Public/   ← Dieses Verzeichnis (Public/App Store Version)
BotVoice/                   ← Private Version (mit eigenen Daten/IP)
```

**Wichtig:** Änderungen am Code immer in `BotVoice/` machen, dann in `SpeakWithOpenClaw-Public/` portieren und pushen.
