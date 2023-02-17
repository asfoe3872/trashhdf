# trashhdf
asdwr
import os
from google.cloud import translate_v2 as translate

os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "path/to/credentials.json"

def translate_text(text):
    client = translate.Client()
    result = client.translate(text, target_language='en')
    return result['translatedText']

text = "這是一段中文文本，將被翻譯為英文。"
translated_text = translate_text(text)
print(translated_text)
