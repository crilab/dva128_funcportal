---
layout: assignment
title: Palindrome Check
difficulty: 1
---
Definition:
{% highlight python %}
def is_palindrome(a: str) -> bool:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera True om strängen *a* är en palindrom (samma framifrån och bakifrån), annars False.

Endast alfanumeriska karaktärer ska beaktas och skiftläget ignoreras (så att exempelvis A och a betraktas som samma tecken).
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return True if the string *a* is a palindrome (the same forwards and backwards), otherwise False.

Only alphanumeric characters should be considered and case should be ignored (so that, for example, A and a are considered the same character).
</div>

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const sentences = [
    "Madam, I'm Adam.",
    "Able was I ere I saw Elba.",
    "A man, a plan, a canal, Panama!",
    "Never odd or even.",
    "Was it a car or a cat I saw?",
    "No lemon, no melon.",
    "Eva, can I see bees in a cave?",
    "Mr. Owl ate my metal worm.",
    "Do geese see God?",
    "Race fast, safe car.",
    "Go hang a salami, I'm a lasagna hog.",
    "Rats live on no evil star.",
    "Ma is as selfless as I am.",
    "Step on no pets.",
    "Madam, in Eden, I'm Adam.",
    "Won't I panic in a pit now?",
    "Taco cat.",
    "Live on time, emit no evil.",
    "Too hot to hoot.",
    "Was it a rat I saw?",
    "Red roses run no risk, sir, on nurses order.",
    "Evil rats on no star live.",
    "Niagara, O roar again!",
    "We panic in a pew.",
    "Doc, note: I dissent. A fast never prevents a fatness. I diet on cod.",
    "Sir, I demand, I am a maid named Iris.",
    "Desserts I stressed.",
    "Was it Eliot's toilet I saw?",
    "Yo, Banana Boy!",
    "Borrow or rob?",
    "Loop pool.",
    "May a moody baby doom a yam?",
    "I did, did I?",
    "Was it a bar or a bat I saw?",
    "No devil lived on.",
    "Drawn onward.",
    "Sir, I'm Iris.",
    "Top spot.",
    "Pull up if I pull up.",
    "Poor Dan is in a droop.",
    "A Santa at NASA.",
    "Sit on a potato pan, Otis.",
    "Ten animals I slam in a net.",
    "Rise to vote, sir.",
    "A dog! A panic in a pagoda!",
    "Euston saw I was not Sue.",
    "Lisa Bonet ate no basil.",
    "Baton, no tab.",
    "Pa's a sap.",
    "Never a foot too far, even.",
    "The cat stretched lazily on the sunny porch.",
    "A gentle breeze rustled the autumn leaves.",
    "She brewed a fresh pot of dark-roast coffee.",
    "The train arrived ten minutes ahead of schedule.",
    "Jason forgot where he parked the rental car.",
    "Lightning flashed across the distant horizon.",
    "They debated politics over dinner and dessert.",
    "Mira sketched a lighthouse in her travel journal.",
    "The library closes early on summer Fridays.",
    "Bees buzzed around the blooming lavender.",
    "I misplaced my keys again this morning.",
    "The violin solo brought the audience to tears.",
    "We hiked until sunset painted the sky orange.",
    "A sudden downpour soaked the city streets.",
    "Sophie mailed postcards from every country she visited.",
    "The baker sprinkled cinnamon on warm muffins.",
    "He solved the crossword without any hints.",
    "The puppy chased its tail in dizzy circles.",
    "Traffic crawled because of construction on the bridge.",
    "Ana planted tomatoes, basil, and rosemary in pots.",
    "The museum unveiled a new contemporary exhibit.",
    "Clouds drifted slowly past the full moon.",
    "She whispered the secret and then laughed.",
    "Marcus booked tickets for the late-night comedy show.",
    "Snowflakes gathered on the cabin windowsill.",
    "The playwright revised the script after rehearsals.",
    "We shared headphones on the long bus ride.",
    "A crisp letter arrived with an unfamiliar stamp.",
    "The chef balanced sweet and spicy flavors perfectly.",
    "Fireworks sparkled above the harbor on New Year's Eve.",
    "He arranged succulents on the rustic shelf.",
    "The detective noticed footprints by the garden gate.",
    "Lila practiced scales on the old upright piano.",
    "The ferry rocked gently as gulls circled overhead.",
    "They binge-watched the entire series in one weekend.",
    "A faint scent of jasmine lingered in the courtyard.",
    "The climber reached the summit just before dawn.",
    "Children giggled while chasing bubbles in the park.",
    "An antique clock chimed softly at midnight.",
    "She bookmarked the recipe for spicy lentil soup.",
    "The astronomer adjusted the telescope's focus.",
    "We toasted marshmallows over glowing embers.",
    "The author signed copies at the local bookstore.",
    "Ocean waves rolled rhythmically onto the shore.",
    "He scribbled ideas on napkins during lunch.",
    "The parade featured dancers in vibrant costumes.",
    "A curious fox trotted across the frosty meadow.",
    "The gardener harvested zucchini and heirloom carrots.",
    "They set up a tent beneath the northern lights.",
    "The choir harmonized beautifully in the stone chapel."
]

const solution = `

def is_palindrome(a):
    p = ''
    for char in a:
        if char.isalpha() or char.isnumeric():
            p += char.lower()
    return p == p[::-1]

`

new Assignment(
    "is_palindrome",
    () => {
        return [
            sentences[randint(0, sentences.length-1)]
        ]
    },
    solution
)

</script>
