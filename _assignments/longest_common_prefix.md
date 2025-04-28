---
layout: assignment
title: Longest Common Prefix
difficulty: 1
---
Implementera:
{% highlight python %}
longest_common_prefix(a: str, b: str) -> str:
{% endhighlight %}

Funktionen ska returnera den längsta gemensamma prefixen av de två strängarna.

Om det inte finns några gemensamma tecken i början, returnera en tom sträng.

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const words = [
  "ability",
  "able",
  "about",
  "above",
  "abroad",
  "absence",
  "absolute",
  "absolutely",
  "abstract",
  "academic",
  "accept",
  "acceptable",
  "accepting",
  "access",
  "accident",
  "accompany",
  "accomplish",
  "according",
  "account",
  "accurate",
  "accurately",
  "accuse",
  "achieve",
  "achievement",
  "acid",
  "acknowledge",
  "acquire",
  "across",
  "act",
  "action",
  "active",
  "actively",
  "activity",
  "actor",
  "actress",
  "actual",
  "actually",
  "adapt",
  "addition",
  "additional",
  "address",
  "adequate",
  "adequately",
  "adjust",
  "administration",
  "admire",
  "adopt",
  "adult",
  "advance",
  "advantage",
  "cycle",
  "cyclist",
  "cycles",
  "cyclic",
  "cyclical",
  "cyclically",
  "cycling",
  "cycleway",
  "cyclone",
  "cyclonic",
  "cyst",
  "cystic",
  "cysts",
  "cytoplasm",
  "cytology",
  "cytosol",
  "cyber",
  "cyberspace",
  "cybersecurity",
  "cyberbullying",
  "cybercrime",
  "cyberpunk",
  "cybernetic",
  "cybernetics",
  "cybercafe",
  "cyberattack",
  "cypress",
  "cynic",
  "cynical",
  "cynicism",
  "cynically",
  "cyborg",
  "cyborgs",
  "cymbal",
  "cymbals",
  "cyclones",
  "cyclists",
  "cycloid",
  "cylinder",
  "cylinders",
  "cylindrical",
  "cyberwar",
  "cyberwarfare",
  "cyan",
  "cyanide",
  "cyanides",
  "cyberstalking",
  "cyberthreat",
  "cytoplasmic",
  "cytoskeleton"
]

const solution = `

def longest_common_prefix(a, b):
    lcp = ''
    for x, y in zip(a, b):
        if x != y:
            break
        lcp += x
    return lcp

`
new Assignment(
    "longest_common_prefix",
    () => {
        return [
            words[randint(0, words.length-1)],
            words[randint(0, words.length-1)]
        ]
    },
    solution
)

</script>
