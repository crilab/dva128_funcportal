---
layout: assignment
title: Filter Even Numbers
difficulty: 3
---
Implementera:
{% highlight python %}
def filter_even(numbers: list[int]) -> list[int]:
{% endhighlight %}

Funktionen ska returnera en ny lista som innehåller alla jämna heltal från listan `numbers` i samma ordning som de förekommer.

<script>

const solution = `

def filter_even(numbers):
    return [n for n in numbers if n % 2 == 0]

`

new Assignment(
    'filter_even',
    () => {
        const numbers_length = 5 + Math.floor(Math.random() * 6)
        const numbers = []
        while (numbers.length < numbers_length)
            numbers.push(-20 + Math.floor(Math.random() * 41))
        return [numbers]
    },
    solution
)

</script>
