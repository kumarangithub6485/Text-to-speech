import json
from gtts import gTTS


def open_json(path):
    '''return a list of dictionaries
    '''
    with open('C:/Users/name/python/EN-63.json', 'r') as file:
        return json.load(file)

data = open_json('./data.json')

#print(data)

text = (data['datasets'][1]['transContent'])
print(text)


tts = gTTS(text = text, lang ='ta')
tts.save("C:/Users/name/Desktop/2020/python/ENG-13-2020-4-30-1200_Shan_1.wav")
print("text converted Successfully")
   
