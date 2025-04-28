---
layout: assignment
title: Prime Checker
difficulty: 1
---
Implementera:
{% highlight python %}
is_prime(n: int) -> bool:
{% endhighlight %}

Funktionen ska returnera `True` om `a` är ett primtal, annars `False`. Du kan förutsätta att `a` alltid är ett positivt heltal större än 1.

<script>

const solution = `

def is_prime(a):
    for i in range(2, a):
        if float(a / i) == int(a / i):
            return False
    return True

`

new Assignment(
    'is_prime',
    () => {
        return [2 + Math.floor(Math.random() * 1000)]
    },
    solution
)

</script>
