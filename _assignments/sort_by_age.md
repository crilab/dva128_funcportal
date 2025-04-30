---
layout: assignment
title: Sort By Age
difficulty: 3
---
Implementera:
{% highlight python %}
def sort_by_age(people: list[dict]) -> list[str]:
{% endhighlight %}

Argumentet *people* är en lista av dictionaries med nycklar:
- **name**: *str*
- **age**: *int*

Funktionen ska returnera en lista med alla namn, sorterade efter ålder i stigande ordning.

Du kan förutsätta att samtliga personer har unika åldrar.

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const names = [
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
]

const solution = `

def sort_by_age(people):
    people_sorted = sorted(people, key=lambda p: p["age"])
    return [person['name'] for person in people_sorted]

`

new Assignment(
    "sort_by_age",
    () => {
        const args = [[]]
        const num_of_people = randint(3, 6)

        const previous_ages = [null]
        const previous_names = [null]
        while (args[0].length < num_of_people) {
            let name = null
            let age = null

            while (true) {
                name = names[randint(0, names.length-1)]
                if (!previous_names.includes(name)) {
                    previous_names.push(name)
                    break
                }
            }

            while (true) {
                age = randint(20, 60)
                if (!previous_ages.includes(age)) {
                    previous_ages.push(age)
                    break
                }
            }

            args[0].push({name, age})
        }
        return args
    },
    solution
)

</script>
