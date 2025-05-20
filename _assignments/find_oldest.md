---
layout: assignment
title: Find Oldest
difficulty: 3
---
Definition:
{% highlight python %}
find_oldest(people: list[dict]) -> str:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Argumentet *people* är en lista av dictionaries med nycklar:
- **name**: *str*
- **age**: *int*

Funktionen ska returnera namnet på den person som är äldst.

Du kan förutsätta att samtliga personer har olika åldrar.
</div>

<div class="english" markdown="1">
Implement the function above.

The argument *people* is a list of dictionaries with keys:
- **name**: *str*
- **age**: *int*

The function should return the name of the person who is oldest.

You can assume that all people have different ages.
</div>

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

def find_oldest(people):
    oldest = people.pop()
    for person in people:
        if oldest["age"] < person["age"]:
            oldest = person
    return oldest['name']

`

new Assignment(
    "find_oldest",
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
