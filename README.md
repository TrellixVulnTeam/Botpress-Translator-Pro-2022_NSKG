## How to use

### 1. Install

```bash
pip install -r requirements.txt
```

### 2. usage

If you want to use Google Translations, create a Google Cloud API key with the Translate API enabled and configure your environment to use it.

Example:
```bash
export GOOGLE_APPLICATION_CREDENTIALS=./google-secret-key.json
```

### Create the translation file:
```bash
python botpress_translator_pro_2022.py --mode=extract --source=en --target=fr --mode=extract --bot botpress_exported_bot.tgz --excel bot_translations_fr.xlsx --google=true
```

If you do not want to use the Google Translate API, disable the automatic translation using the `--google=false` flag.

You can manually edit the translation file using Excel or LibreOffice (or whatever else). Some rows are protected and shouldn't be edited.

### Create a new chatbot archive:
```bash
python botpress_translator_pro_2022.py --mode=pack --bot botpress_exported_bot.tgz --excel bot_translations_fr.xlsx --new bot_translated.tgz
```