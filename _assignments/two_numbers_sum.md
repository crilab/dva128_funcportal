---
layout: assignment
title: Two Numbers Sum
difficulty: 0
---
Definition:
{% highlight python %}
def add(a: float, b: float) -> float:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera summan av de två flyttalen.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return the sum of the two floating-point numbers.
</div>

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
            args.push((Math.floor(Math.random() * 200000) - 100000) / 100)
        }
        return args
    },
    solution
)

</script>
