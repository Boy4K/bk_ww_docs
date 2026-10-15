# Translations

Texts live in `locales/`: `it.json` and `en.json`. Choose the language with `Config.Locale`.

To add a language:

1. Copy `en.json` to e.g. `es.json`.
2. Translate the values (keep the keys and the `%s` / `%d` / `{id}` placeholders).
3. Set `Config.Locale = 'es'` and restart.

| Section | Used for |
| --- | --- |
| `server` | notifications sent by the server |
| `game` | ox_target labels and on-screen help |
| `nui` | the panel |
| `poster` | text printed on WANTED posters |
| `newspaper` | front page and reader text, article categories |
| `log` | Discord logs |
