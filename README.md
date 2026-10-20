# Utter

Hold a key, speak, release — the text lands where your caret is, in any Windows app.

Utter is a small tray program for Windows 10 and 11. No account with us, no server of ours: speech goes straight from your computer to the speech service you connect.

## Get it

1. Download `Utter-Setup.exe` from the [latest release](https://github.com/1lyakey/utter-releases/releases/latest).
2. Run it and press "Install the program". Utter copies itself to `%LOCALAPPDATA%\Utter` and starts from the tray.
3. The first-run window walks you through three steps: the key, speech, a box to try it in.

### "Windows protected your PC"

Utter is not code-signed yet, so Windows SmartScreen may stop the first start. Click **More info**, then **Run anyway**. To check the file is the one published here, compare its SHA-256 with `sha256` in this release's `update.json`:

```powershell
Get-FileHash .\Utter-Setup.exe -Algorithm SHA256
```

## Connect speech

One of these is enough:

- **Groq — free.** Get a key at [console.groq.com/keys](https://console.groq.com/keys), then tray icon → "Groq key". Speech is `whisper-large-v3`; the text appears after you release the key. The free tier has daily limits set by Groq.
- **xAI.** Your xAI API key (console.x.ai → API keys), tray icon → "xAI key". Speech is `grok-voice-transcribe-2.0`, with the words on screen while you speak.

Keys stay on your computer, encrypted for your Windows account.

## Use it

- Hold the key (Right Ctrl by default, ё on a Russian keyboard; Pause, a letter or another key in Settings), speak, release.
- A short tap or Esc cancels while nothing is in the window yet.
- Double tap: dictate hands-free; the next tap inserts.
- Polishing (on the Text tab) fixes punctuation and small slips with a model you choose; the first draft is inserted at once and swapped quietly when the polished text is ready.
- Say "comma", "period", "new line", "new paragraph", "delete last word" — they become marks and actions.

## Privacy

What leaves your computer and what stays: [PRIVACY.md](PRIVACY.md).

## Updates

Tray icon → "New version" checks this repository and installs a newer `Utter-Setup.exe` after checking its SHA-256.
