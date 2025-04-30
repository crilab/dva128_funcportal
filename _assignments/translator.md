---
layout: assignment
title: Translator
difficulty: 2
---
Implementera:
{% highlight python %}
def translate(sentence: str, glossary: dict[str, str]) -> str:
{% endhighlight %}

Argumentet *glossary* är ett dictionary där varje nyckel är ett svenskt ord och värdet dess engelska direktöversättning.

Funktionen ska returnera en sträng där varje svenskt ord i **sentence** direköversatts enligt **glossary**.

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

function shuffleObjectKeys(obj) {
    const entries = Object.entries(obj)
    const shuffled = {}

    while (0 < entries.length) {
        const index = Math.floor(Math.random() * entries.length)
        const [key, value] = entries.splice(index, 1)[0]
        shuffled[key] = value
    }

    return shuffled
}

const sentences = [
  {
    "sentence": "hunden skällde på hunden i fönstret och jag blev förvånad",
    "glossary": {
      "hunden": "the dog",
      "skällde": "barked",
      "på": "at",
      "i": "in",
      "fönstret": "the mirror",
      "och": "and",
      "jag": "i",
      "blev": "was",
      "förvånad": "surprised"
    }
  },
  {
    "sentence": "katten sprang upp i rummet och musen rymde",
    "glossary": {
      "katten": "the cat",
      "sprang": "ran",
      "upp": "up",
      "i": "in",
      "rummet": "the room",
      "och": "and",
      "musen": "the mouse",
      "rymde": "escaped"
    }
  },
  {
    "sentence": "flickan gick till parken med sin hund",
    "glossary": {
      "flickan": "the girl",
      "gick": "walked",
      "till": "to",
      "parken": "the park",
      "med": "with",
      "sin": "her",
      "hund": "dog"
    }
  },
  {
    "sentence": "pojken lekte med en boll i trädgården",
    "glossary": {
      "pojken": "the boy",
      "lekte": "played",
      "med": "with",
      "en": "a",
      "boll": "ball",
      "i": "in",
      "trädgården": "the garden"
    }
  },
  {
    "sentence": "katten sov under soffan hela dagen",
    "glossary": {
      "katten": "the cat",
      "sov": "slept",
      "under": "under",
      "soffan": "the sofa",
      "hela": "the whole",
      "dagen": "day"
    }
  },
  {
    "sentence": "de simmade i sjön tills solen gick ner",
    "glossary": {
      "de": "they",
      "simmade": "swam",
      "i": "in",
      "sjön": "the lake",
      "tills": "until",
      "solen": "the sun",
      "gick": "went",
      "ner": "down"
    }
  },
  {
    "sentence": "vi cyklade till skolan varje dag",
    "glossary": {
      "vi": "we",
      "cyklade": "cycled",
      "till": "to",
      "skolan": "the school",
      "varje": "every",
      "dag": "day"
    }
  },
  {
    "sentence": "hon skrev ett brev till sin vän",
    "glossary": {
      "hon": "she",
      "skrev": "wrote",
      "ett": "a",
      "brev": "letter",
      "till": "to",
      "sin": "her",
      "vän": "friend"
    }
  },
  {
    "sentence": "de byggde en koja i skogen",
    "glossary": {
      "de": "they",
      "byggde": "built",
      "en": "a",
      "koja": "hut",
      "i": "in",
      "skogen": "the forest"
    }
  },
  {
    "sentence": "pappan lagade mat i det lilla huset",
    "glossary": {
      "pappan": "the father",
      "lagade": "cooked",
      "mat": "food",
      "i": "in",
      "det": "the",
      "lilla": "small",
      "huset": "house"
    }
  },
  {
    "sentence": "barnet ritade en bil med krita",
    "glossary": {
      "barnet": "the child",
      "ritade": "drew",
      "en": "a",
      "bil": "car",
      "med": "with",
      "krita": "crayon"
    }
  },
  {
    "sentence": "en fisk simmade snabbt i vattnet",
    "glossary": {
      "en": "a",
      "fisk": "fish",
      "simmade": "swam",
      "snabbt": "quickly",
      "i": "in",
      "vattnet": "the water"
    }
  },
  {
    "sentence": "en man satt vid elden och drack te",
    "glossary": {
      "en": "a",
      "man": "man",
      "satt": "sat",
      "vid": "by",
      "elden": "the fire",
      "och": "and",
      "drack": "drank",
      "te": "tea"
    }
  },
  {
    "sentence": "huset hade vita fönster med blommor",
    "glossary": {
      "huset": "the house",
      "hade": "had",
      "vita": "white",
      "fönster": "windows",
      "med": "with",
      "blommor": "flowers"
    }
  },
  {
    "sentence": "barnen sjöng en visa i rummet",
    "glossary": {
      "barnen": "the children",
      "sjöng": "sang",
      "en": "a",
      "visa": "song",
      "i": "in",
      "rummet": "the room"
    }
  },
  {
    "sentence": "hon hittade en bok under sängen",
    "glossary": {
      "hon": "she",
      "hittade": "found",
      "en": "a",
      "bok": "book",
      "under": "under",
      "sängen": "the bed"
    }
  },
  {
    "sentence": "farfar fixade cykeln i garaget",
    "glossary": {
      "farfar": "grandfather",
      "fixade": "fixed",
      "cykeln": "the bike",
      "i": "in",
      "garaget": "the garage"
    }
  },
  {
    "sentence": "de satt tysta vid bordet och log",
    "glossary": {
      "de": "they",
      "satt": "sat",
      "tysta": "quiet",
      "vid": "at",
      "bordet": "the table",
      "och": "and",
      "log": "smiled"
    }
  },
  {
    "sentence": "lampan lyste svagt i natten",
    "glossary": {
      "lampan": "the lamp",
      "lyste": "shone",
      "svagt": "dimly",
      "i": "in",
      "natten": "the night"
    }
  },
  {
    "sentence": "en kvinna gick tyst genom staden",
    "glossary": {
      "en": "a",
      "kvinna": "woman",
      "gick": "walked",
      "tyst": "silently",
      "genom": "through",
      "staden": "the city"
    }
  },
  {
    "sentence": "vinden susade i trädens kronor",
    "glossary": {
      "vinden": "the wind",
      "susade": "whispered",
      "i": "in",
      "trädens": "the trees'",
      "kronor": "crowns"
    }
  },
  {
    "sentence": "isbjörn gick ensam över isen",
    "glossary": {
      "isbjörn": "polar bear",
      "gick": "walked",
      "ensam": "alone",
      "över": "across",
      "isen": "the ice"
    }
  },
  {
    "sentence": "en liten båt gled ut i sjön",
    "glossary": {
      "en": "a",
      "liten": "small",
      "båt": "boat",
      "gled": "glided",
      "ut": "out",
      "i": "into",
      "sjön": "the lake"
    }
  },
  {
    "sentence": "flickan tappade sin hatt i vinden",
    "glossary": {
      "flickan": "the girl",
      "tappade": "dropped",
      "sin": "its",
      "hatt": "hat",
      "i": "in",
      "vinden": "the wind"
    }
  },
  {
    "sentence": "en myra bar ett blad hem",
    "glossary": {
      "en": "an",
      "myra": "ant",
      "bar": "carried",
      "ett": "a",
      "blad": "leaf",
      "hem": "home"
    }
  },
  {
    "sentence": "en pojke skrattade i regnet",
    "glossary": {
      "en": "a",
      "pojke": "boy",
      "skrattade": "laughed",
      "i": "in",
      "regnet": "the rain"
    }
  },
  {
    "sentence": "boken låg kvar vid sängen hela natten",
    "glossary": {
      "boken": "the book",
      "låg": "lay",
      "kvar": "left",
      "vid": "by",
      "sängen": "the bed",
      "hela": "all",
      "natten": "the night"
    }
  },
  {
    "sentence": "de tittade upp mot himlen i tystnad",
    "glossary": {
      "de": "they",
      "tittade": "looked",
      "upp": "up",
      "mot": "toward",
      "himlen": "the sky",
      "i": "in",
      "tystnad": "silence"
    }
  },
  {
    "sentence": "en fågel satt ensam i ett träd",
    "glossary": {
      "en": "a",
      "fågel": "bird",
      "satt": "sat",
      "ensam": "alone",
      "i": "in",
      "ett": "a",
      "träd": "tree"
    }
  },
  {
    "sentence": "mamma gav mig en bok att läsa",
    "glossary": {
      "mamma": "mom",
      "gav": "gave",
      "mig": "me",
      "en": "a",
      "bok": "book",
      "att": "to",
      "läsa": "read"
    }
  },
  {
    "sentence": "han gick hem med sin väska",
    "glossary": {
      "han": "he",
      "gick": "walked",
      "hem": "home",
      "med": "with",
      "sin": "his",
      "väska": "bag"
    }
  },
  {
    "sentence": "vi satt ute och lyssnade till regnet",
    "glossary": {
      "vi": "we",
      "satt": "sat",
      "ute": "outside",
      "och": "and",
      "lyssnade": "listened",
      "till": "to",
      "regnet": "the rain"
    }
  },
  {
    "sentence": "barnet ritade ett hus med rök",
    "glossary": {
      "barnet": "the child",
      "ritade": "drew",
      "ett": "a",
      "hus": "house",
      "med": "with",
      "rök": "smoke"
    }
  },
  {
    "sentence": "de lämnade platsen utan ljud",
    "glossary": {
      "de": "they",
      "lämnade": "left",
      "platsen": "the place",
      "utan": "without",
      "ljud": "sound"
    }
  },
  {
    "sentence": "en katt smög tyst genom rummet",
    "glossary": {
      "en": "a",
      "katt": "cat",
      "smög": "snuck",
      "tyst": "quietly",
      "genom": "through",
      "rummet": "the room"
    }
  },
  {
    "sentence": "ljuset kom in genom fönstret",
    "glossary": {
      "ljuset": "the light",
      "kom": "came",
      "in": "in",
      "genom": "through",
      "fönstret": "the window"
    }
  },
  {
    "sentence": "pappan bar barnet till bilen",
    "glossary": {
      "pappan": "the father",
      "bar": "carried",
      "barnet": "the child",
      "till": "to",
      "bilen": "the car"
    }
  },
  {
    "sentence": "de sprang i regnet med glädje",
    "glossary": {
      "de": "they",
      "sprang": "ran",
      "i": "in",
      "regnet": "the rain",
      "med": "with",
      "glädje": "joy"
    }
  }
]

const solution = `

def translate(sentence, glossary):
    sentence = sentence.split()
    return ' '.join(glossary[word] for word in sentence)

`

new Assignment(
    "translate",
    () => {
        const s = sentences[randint(0, sentences.length-1)]
        return [
            s.sentence,
            shuffleObjectKeys(s.glossary)
        ]
    },
    solution
)

</script>
