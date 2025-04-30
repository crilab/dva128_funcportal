---
layout: assignment
title: Square Each Number
difficulty: 3
---
Implementera:
{% highlight python %}
def map_square(numbers: list[int]) -> list[int]:
{% endhighlight %}

Funktionen ska returnera en ny lista där varje element är kvadraten av motsvarande element i den ursprungliga listan.

<script>

const solution = `

def map_square(numbers):
    return [n**2 for n in numbers]

`

new Assignment(
    'map_square',
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
