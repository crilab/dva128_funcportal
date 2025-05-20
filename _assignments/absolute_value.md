---
layout: assignment
title: Absolute Value
difficulty: 0
---
Definition:
{% highlight python %}
absolute_value(a: float) -> float:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera absolutbeloppet av det givna flyttalet.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return the absolute value of the given floating-point number.
</div>

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
