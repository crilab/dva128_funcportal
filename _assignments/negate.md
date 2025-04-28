---
layout: assignment
title: Negate Number
difficulty: 0
---
Implementera:
{% highlight python %}
negate(a: float) -> float:
{% endhighlight %}

Funktionen ska returnera talets negation (d.v.s. talet med omvänt tecken).

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
