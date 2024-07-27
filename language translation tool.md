#codealpha_tasks
from googletrans import Translator, LANGUAGES

def translate_text(text, dest_lang):
    translator = Translator()
    translated = translator.translate(text, dest=dest_lang)
    return translated.text

def main():
    # List available languages
    print("Available languages:")
    for lang_code, lang_name in LANGUAGES.items():
        print(f"{lang_code}: {lang_name}")

    # Take user input
    text = input("Enter the text to be translated: ")
    dest_lang = input("Enter the language code to translate to: ")

    # Check if the provided language code is valid
    if dest_lang in LANGUAGES:
        # Translate text
        translated_text = translate_text(text, dest_lang)
        print(f"Translated text: {translated_text}")
    else:
        print("Invalid language code. Please try again.")

if __name__ == "__main__":
    main()
