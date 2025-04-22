---
layout: assignment
title: Two Numbers Sum
difficulty: 0
---
Implementera:
{% highlight python %}
add(a: float, b: float) -> float:
{% endhighlight %}

Funktionen ska returnera summan av de två flyttalen.

<script>

const solution = `

def add(a, b):
    return a + b

`
new Assignment(
    'add',
    () => {
        const args = []
        while (args.length < 2) {
            args.push(Math.floor(Math.random() * 2000) - 1000)
        }
        return args
    },
    solution
)

</script>
