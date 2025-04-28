---
layout: assignment
title: Absolute Value
difficulty: 0
---
Implementera:
{% highlight python %}
absolute_value(a: float) -> float:
{% endhighlight %}

Funktionen ska returnera absolutbeloppet av det givna flyttalet.

<script>

const solution = `

def absolute_value(a):
    return abs(a)

`

new Assignment(
    'absolute_value',
    () => {
        return [(Math.floor(Math.random() * 200001) - 100000) / 100]
    },
    solution
)

</script>
