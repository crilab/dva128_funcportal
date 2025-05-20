---
layout: assignment
title: Longest Common Suffix
difficulty: 1
---
Definition:
{% highlight python %}
longest_common_suffix(a: str, b: str) -> str:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera den längsta gemensamma suffixen (ändelsen) av två strängar.

Om ingen gemensam suffix finns, returnera en tom sträng.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return the longest common suffix of two strings.

If no common suffix exists, return an empty string.
</div>

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const words = [
  "apple",
  "breeze",
  "cake",
  "dance",
  "edge",
  "flame",
  "glove",
  "hope",
  "ice",
  "joke",
  "kite",
  "love",
  "mouse",
  "noise",
  "olive",
  "plate",
  "quote",
  "rise",
  "smile",
  "time",
  "urge",
  "vase",
  "wave",
  "xyleme",
  "yoke",
  "zone",
  "abode",
  "bribe",
  "choke",
  "dive",
  "elope",
  "freeze",
  "gauge",
  "hinge",
  "ignite",
  "jive",
  "knave",
  "lease",
  "mope",
  "niche",
  "ooze",
  "probe",
  "queue",
  "rogue",
  "spire",
  "truce",
  "use",
  "vice",
  "whale",
  "axe",
  "base",
  "clause",
  "drape",
  "evade",
  "fable",
  "gorge",
  "hare",
  "incise",
  "jade",
  "knife",
  "lounge",
  "mince",
  "note",
  "ounce",
  "pace",
  "quiche",
  "rattle",
  "scribe",
  "tense",
  "uncle",
  "verge",
  "while",
  "exile",
  "yare",
  "agape",
  "bane",
  "clothe",
  "deuce",
  "emerge",
  "flute",
  "grade",
  "house",
  "idle",
  "jangle",
  "kneel",
  "lance",
  "maze",
  "nurse",
  "opine",
  "pause",
  "quite",
  "reuse",
  "sage",
  "tale",
  "unique",
  "value",
  "wedge",
  "xeroxable",
  "yankee",
  "zeppole",
  "apples",
  "bananas",
  "cats",
  "dogs",
  "eggs",
  "frogs",
  "grapes",
  "hats",
  "ideas",
  "jokes",
  "knives",
  "lemons",
  "maps",
  "nuts",
  "orbits",
  "pencils",
  "quilts",
  "rivers",
  "stones",
  "trees",
  "umbrellas",
  "vases",
  "whales",
  "x-rays",
  "zebras"
]

const solution = `

def longest_common_suffix(a, b):
    a = a[::-1]
    b = b[::-1]
    lcs = ''
    for x, y in zip(a, b):
        if x != y:
            break
        lcs += x
    return lcs[::-1]

`
new Assignment(
    "longest_common_suffix",
    () => {
        return [
            words[randint(0, words.length-1)],
            words[randint(0, words.length-1)]
        ]
    },
    solution
)

</script>
