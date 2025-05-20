---
layout: assignment
title: Square Each Number
difficulty: 3
---
Definition:
{% highlight python %}
def map_square(numbers: list[int]) -> list[int]:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera en ny lista där varje element är kvadraten av motsvarande element i den ursprungliga listan.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return a new list where each element is the square of the corresponding element in the original list.
</div>

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
