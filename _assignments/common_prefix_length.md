---
layout: assignment
title: Common Prefix Length
difficulty: 1
---
Definition:
{% highlight python %}
common_prefix_length(a: str, b: str) -> int:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera längden på det längsta gemensamma prefixet av de två strängarna.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return the length of the longest common prefix of the two strings.
</div>

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const words = [
  "adapt",
  "addict",
  "address",
  "adjoin",
  "adjust",
  "admire",
  "admit",
  "adopt",
  "adore",
  "adorn",
  "advance",
  "advantage",
  "adventure",
  "advertise",
  "advise",
  "adviser",
  "advocate",
  "adage",
  "addition",
  "additional",
  "adhesive",
  "adjacent",
  "adjective",
  "adjudicate",
  "adjunct",
  "administer",
  "administration",
  "administrative",
  "admiration",
  "adolescent",
  "adoration",
  "adulthood",
  "adulterate",
  "adulteration",
  "adult",
  "adventureland",
  "adventurous",
  "adversity",
  "adversary",
  "advertise",
  "advertisement",
  "advertiser",
  "advising",
  "advisory",
  "advocacy",
  "adynamic",
  "adaption",
  "adaptable",
  "adaptation",
  "adaptor",
  "adept",
  "addicting",
  "addicted",
  "addiction",
  "additionally",
  "adhesiveness",
  "adjourn",
  "adjudicator",
  "adjudication",
  "adjustment",
  "admittance",
  "admissible",
  "admission",
  "admiring",
  "admiringly",
  "adoption",
  "adopting",
  "adopter",
  "adorable",
  "adorably",
  "adoration",
  "adroit",
  "adroitness",
  "adscript",
  "adsorb",
  "adsorption",
  "adulate",
  "adulation",
  "adulatory",
  "adulterant",
  "adulterer",
  "adulteress",
  "adultery",
  "adulthood",
  "advancement",
  "advancing",
  "advantaged",
  "adversarial",
  "adversative",
  "advert",
  "advertence",
  "advertency",
  "advertisee",
  "advertising",
  "advertorial",
  "advisability",
  "advisable",
  "advisee",
  "advisement",
  "advisor",
  "cyan",
  "cyanide",
  "cyborg",
  "cyber",
  "cyberspace",
  "cybersecurity",
  "cyberattack",
  "cyberbully",
  "cyberbullying",
  "cybercrime",
  "cybercafe",
  "cybernetic",
  "cybernetics",
  "cypher",
  "cycling",
  "cyclist",
  "cyclone",
  "cyclonic",
  "cyclops",
  "cyclotron",
  "cylinder",
  "cylindrical",
  "cygnet",
  "cynic",
  "cynicism"
]

const solution = `

def common_prefix_length(a, b):
    cpl = 0
    for x, y in zip(a, b):
        if x != y:
            break
        cpl += 1
    return cpl

`
new Assignment(
    "common_prefix_length",
    () => {
        return [
            words[randint(0, words.length-1)],
            words[randint(0, words.length-1)]
        ]
    },
    solution
)

</script>
