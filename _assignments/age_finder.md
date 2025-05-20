---
layout: assignment
title: Age Finder
difficulty: 3
---
Definition:
{% highlight python %}
def find(people: list[dict], age: int) -> list[str]:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Argumentet *people* är en lista av dictionaries med nycklar:
- **name**: *str*
- **age**: *int*

Funktionen ska returnera en lista med namnen på alla personer vars ålder är exakt lika med funktionens argument *age*.
</div>

<div class="english" markdown="1">
Implement the function above.

The argument *people* is a list of dictionaries with keys:
- **name**: *str*
- **age**: *int*

The function should return a list of the names of all people whose age is exactly equal to the function's argument *age*.
</div>

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const names = `[
  "Erik",
  "Anna",
  "Johan",
  "Elsa",
  "Lars",
  "Sara",
  "Oskar",
  "Maja",
  "Nils",
  "Emilia"
]`

const solution = `

def find(people, age):
    result = []
    for person in people:
        if person["age"] == age:
            result.append(person["name"])
    return result

`
new Assignment(
    "find",
    () => {
        let new_names = JSON.parse(names)
        const args = [[], randint(30,32)]
        const args_length = randint(3, 6)
        while (args[0].length < args_length) {
            args[0].push({
                name: new_names.splice(
                    randint(0, new_names.length-1),
                    1
                )[0],
                age: randint(30,32)
            })
        }
        return args
    },
    solution
)

</script>
