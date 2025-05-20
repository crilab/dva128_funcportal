---
layout: assignment
title: Prime Checker
difficulty: 1
---
Definition:
{% highlight python %}
def is_prime(n: int) -> bool:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera `True` om *a* är ett primtal, annars `False`. Du kan förutsätta att *a* alltid är ett positivt heltal större än 1.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return `True` if *n* is a prime number, otherwise `False`. You can assume that *n* is always a positive integer greater than 1.
</div>

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
