---
layout: assignment
title: Even Number Check
difficulty: 0
---
Definition:
{% highlight python %}
is_even(a: int) -> bool:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera `True` om heltalet *a* är jämnt (dvs. delbart med 2), annars `False`.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return `True` if the integer *a* is even (i.e., divisible by 2), otherwise `False`.
</div>

<script>

const solution = `

def is_even(a):
    return a % 2 == 0

`

new Assignment(
    'is_even',
    () => {
        return [Math.floor(Math.random() * 2001) - 1000]
    },
    solution
)

</script>
