---
layout: assignment
title: Filter Even Numbers
difficulty: 3
---
Definition:
{% highlight python %}
filter_even(numbers: list[int]) -> list[int]:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera en ny lista som innehåller alla jämna heltal från listan `numbers` i samma ordning som de förekommer.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return a new list containing all even integers from the list `numbers` in the same order as they appear.
</div>

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
