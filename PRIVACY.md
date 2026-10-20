# Utter privacy

Utter has no server of its own. It talks only to the services you connect.

## What leaves your computer

- **Sound, while you hold the key.** It goes to the speech service you chose on the Speech tab:
  - Groq (`whisper-large-v3`), after you release the key, in one request;
  - or xAI (`grok-voice-transcribe-2.0`), while you speak.
- **The recognized text, when polishing is on.** It goes to the polish service you chose on the Text tab (Groq, xAI, OpenAI, Anthropic, Google, a local Ollama or LM Studio, and others). With polishing off, the text goes nowhere.
- **Words from your dictionary.** They go along with speech requests, so the service spells them right.
- **An update check.** Utter reads `update.json` from the public `1lyakey/utter-releases` repository on GitHub. Nothing about you is sent.

What each service does with the data is set by that service's own terms. Free tiers may use what you send to improve their products; read their terms before you connect.

## What stays on your computer

Everything below lives in `%LOCALAPPDATA%\Utter`:

- `settings.json` — settings, your dictionary and snippets, and the history of the last 40 phrases. History tab → "Keep the history on this computer" turns history off; "Clear the history" erases it. Both take effect on Save.
- `keys.bin` and `auth.bin` — API keys and the SuperGrok sign-in, encrypted with Windows DPAPI for your Windows account.
- `diag.log` — the timing log: times, lengths, model names, never the text. Off for new installs. Turning it off on the History tab deletes the file.
- `crash-*.txt` and `last-error.txt` — what failed and where in the code, never the text you dictated.

Utter records sound only while you dictate: from the key press to its release, or from a double tap to the next tap. It does not keep the sound after the phrase is recognized.

---

# Utter и приватность

У Utter нет своего сервера. Программа говорит только с сервисами, которые ты подключил.

## Что уходит с компьютера

- **Звук, пока клавиша зажата.** Уходит в сервис речи, выбранный на вкладке «Речь»:
  - Groq (`whisper-large-v3`) — одним запросом после отпускания клавиши;
  - или xAI (`grok-voice-transcribe-2.0`) — пока говоришь.
- **Распознанный текст, если правка включена.** Уходит в сервис правки с вкладки «Текст» (Groq, xAI, OpenAI, Anthropic, Google, локальные Ollama или LM Studio и другие). С выключенной правкой текст никуда не уходит.
- **Слова из словаря.** Идут вместе с запросом речи, чтобы сервис писал их правильно.
- **Проверка обновления.** Utter читает `update.json` из публичного репозитория `1lyakey/utter-releases` на GitHub. О тебе ничего не отправляется.

Что сервис делает с данными, решают его условия. Бесплатные тарифы могут использовать присланное для улучшения своих продуктов — прочитай их условия до подключения.

## Что остаётся на компьютере

Всё ниже лежит в `%LOCALAPPDATA%\Utter`:

- `settings.json` — настройки, словарь, замены и история последних 40 фраз. Вкладка «История» → «Хранить историю на этом компьютере» выключает историю; «Очистить историю» стирает её. И то и другое — после «Сохранить».
- `keys.bin` и `auth.bin` — ключи и вход SuperGrok, зашифрованы Windows DPAPI под твою учётную запись.
- `diag.log` — журнал замеров: время, длина, имя модели, без текста. У новой установки выключен. Выключение на вкладке «История» удаляет файл.
- `crash-*.txt` и `last-error.txt` — что сломалось и где в коде, без продиктованного текста.

Utter пишет звук только пока ты диктуешь: от нажатия клавиши до отпускания или от двойного тапа до следующего тапа. Звук после распознавания фразы не хранится.
