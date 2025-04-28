---
layout: assignment
title: Even Number Check
difficulty: 0
---
Implementera:
{% highlight python %}
is_even(a: int) -> bool:
{% endhighlight %}

Funktionen ska returnera `True` om heltalet `a` är jämnt (dvs. delbart med 2), annars `False`.

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
