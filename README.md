# deneme1

## Projemin konusu:

## Proje türü: 


from flask import Flask
import random

app = Flask(__name__)


yazıTura = ['yazı' , 'tura']

@app.route("/selam")
def hello_world():
    return f'<h1>{random.choice(yazıTura)}</h1>'

@app.route("/")
def hello():
    return '<a href="/selam">Selam yazı mı tura MI ?</a>'

app.run(debug=True)
