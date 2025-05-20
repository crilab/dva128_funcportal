---
layout: assignment
title: Negate Number
difficulty: 0
---
Definition:
{% highlight python %}
def negate(a: float) -> float:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera talets negation (d.v.s. talet med omvänt tecken).
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return the negation of the number (i.e., the number with the opposite sign).
</div>

<script>

const solution = `

def negate(a):
    return -a

`

new Assignment(
    'negate',
    () => {
        return [(Math.floor(Math.random() * 200001) - 100000) / 100]
    },
    solution
)

</script>
