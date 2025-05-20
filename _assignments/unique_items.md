---
layout: assignment
title: Unique Items
difficulty: 2
---
Definition:
{% highlight python %}
def unique(*items) -> list:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen tar emot ett godtyckligt antal argument och returnerar en lista där varje unikt värde endast förekommer en gång, i den ordning de skickades in.

Du kan utgå från att inparametrarna endast är av typerna:
- str
- int
- float
</div>

<div class="english" markdown="1">
Implement the function above.

The function accepts an arbitrary number of arguments and returns a list where each unique value appears only once, in the order they were passed in.

You can assume that the input parameters are only of the types:
- str
- int
- float
</div>

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
