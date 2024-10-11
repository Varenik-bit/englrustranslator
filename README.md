# englrustranslator
from translate import Translator

user_language = input('Напишите "1" для перевода с русского на английский, "2" для перевода с английского на русский: ')

def translator(lang1, lang2):
    translator = Translator(from_lang=lang1, to_lang=lang2)
    user_word = input('Введите слово или предложение для перевода: ')
    global translation
    translation = translator.translate(user_word)

if user_language == '1':
    translator('russian', 'english')
else:
    translator('english', 'russian')

print(translation)
