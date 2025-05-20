---
layout: assignment
title: Find Last
difficulty: 3
---
Definition:
{% highlight python %}
def find_last(people: list[dict], age: int) -> str:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Argumentet *people* är en lista av dictionaries med nycklar:
- **name**: *str*
- **age**: *int*

Funktionen ska returnera namnet på den sista personen vars ålder matchar med inparametern *age*.

Om ingen match hittas, returnera en tom sträng.
</div>

<div class="english" markdown="1">
Implement the function above.

The argument *people* is a list of dictionaries with keys:
- **name**: *str*
- **age**: *int*

The function should return the name of the last person whose age matches the input parameter *age*.

If no match is found, return an empty string.
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

def find_last(people, age):
    match = ''
    for person in people:
        if person['age'] == age:
            match = person['name']
    return match

`

new Assignment(
    "find_last",
    () => {
        const people = []
        const num_of_people = randint(5, 8)

        const previous_names = [null]
        while (people.length < num_of_people) {
            let name = null

            while (true) {
                name = names[randint(0, names.length-1)]
                if (!previous_names.includes(name)) {
                    previous_names.push(name)
                    break
                }
            }

            let age = randint(50, 52)

            people.push({name, age})
        }
        let age_to_find = people[randint(0, people.length-1)].age
        if (Math.random() < 0.25)
            age_to_find = randint(20, 80)
        return [people, age_to_find]
    },
    solution
)

</script>
