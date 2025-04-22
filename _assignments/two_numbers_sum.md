---
layout: assignment
title: Two Numbers Sum
difficulty: 0
---
Definiera en funktion **double** som tar två heltal som argument.

Funktionen ska returnera summan av de två heltalen (som heltal).

<script>

const solution = `

def double(a, b):
    return a + b

`
new Assignment(
    'double',
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
