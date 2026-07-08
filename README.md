# Language Translator UI

An interactive text translator built in a Jupyter/Google Colab notebook using `ipywidgets`. It lets you type text, pick a target language, translate it, listen to the translation via text-to-speech, and copy the result to your clipboard.

## Features

- **Text Input** — a textarea widget to type or paste the text you want translated.
- **Language Selection** — a dropdown to choose the target language (English, Spanish, French, German, Italian, Japanese, Korean, Chinese (Simplified)).
- **Translation** — translates the input text using the `googletrans` library (an unofficial wrapper around Google Translate).
- **Text-to-Speech (optional)** — reads the translated text aloud using `gTTS` (Google Text-to-Speech).
- **Copy to Clipboard (optional)** — copies the translated text to your clipboard with one click.

## Requirements

- Python 3
- Jupyter Notebook, JupyterLab, or Google Colab
- Packages (installed automatically by the notebook's `!pip install` cells):
  - `ipywidgets`
  - `googletrans==4.0.0-rc1`
  - `gTTS`

## How to Use

1. Open `Task_1_ipynb.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
2. Run the cells **in order, from top to bottom**:
   1. **Set up the UI** — creates the text input and language dropdown widgets.
   2. **Integrate Translation API** — installs `googletrans` and defines the translation logic; displays the "Translate" button.
   3. **Add Text-to-Speech (Optional)** — installs `gTTS` and adds a "Speak Translated Text" button.
   4. **Add Copy Feature (Optional)** — adds a "Copy Translated Text" button.
3. Type text into the textarea, choose a target language from the dropdown, and click **Translate**.
4. Optionally, click **Speak Translated Text** to hear the translation, or **Copy Translated Text** to copy it to your clipboard.

## Notes

- The clipboard-copy feature relies on browser JavaScript (`navigator.clipboard.writeText`) and works best in Colab or a browser-based Jupyter session — it may not work in all local environments.
- `googletrans` is an unofficial library that scrapes Google Translate; it can occasionally break or rate-limit if Google changes its internal API.
- The notebook contains a few duplicated cells (the Text-to-Speech and Copy Feature sections repeat); re-running duplicate cells is harmless but not required — running each section once is enough.

## License

For educational/demo purposes.
