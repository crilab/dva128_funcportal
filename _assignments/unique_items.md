---
layout: assignment
title: Unique Items
difficulty: 2
---
Implementera:
{% highlight python %}
def unique(*items) -> list:
{% endhighlight %}

Funktionen tar emot ett godtyckligt antal argument och returnerar en lista där varje unikt värde endast förekommer en gång, i den ordning de skickades in.

Du kan utgå från att inparametrarna endast är av typerna:
- str
- int
- float

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const elements = [
    'A',
    'B',
    'C',
    'D',
    -2,
    -1,
    1,
    2,
    -2.5,
    -1.5,
    1.5,
    2.5
]

const solution = `

def unique(*items):
    unique = []
    for item in items:
        if item not in unique:
            unique.append(item)
    return unique

`

new Assignment(
    "unique",
    () => {
        const args = []
        const num_of_args = randint(10,14)
        while (args.length < num_of_args) {
            args.push(elements[randint(0, elements.length-1)])
        }
        return args
    },
    solution
)

</script>
