---
layout: assignment
title: Concatenate Strings with Spaces
difficulty: 1
---
Definition:
{% highlight python %}
concat_with_space(*strings: str) -> str:
{% endhighlight %}

<div class="swedish" markdown="1">
Implementera funktionen ovan.

Funktionen ska returnera en sträng där alla inparametrar är hopfogade med ett mellanslag emellan.
</div>

<div class="english" markdown="1">
Implement the function above.

The function should return a string where all input parameters are concatenated with a space in between.
</div>

<script>

function randint(a, b) {
    return Math.floor(Math.random() * (b - a + 1)) + a
}

const sentences = [
    ['The', 'sun', 'rose', 'early', 'over', 'the', 'quiet', 'mountain', 'village.'],
    ['She', 'baked', 'a', 'chocolate', 'cake', 'for', 'her', 'sister\'s', 'birthday.'],
    ['The', 'children', 'played', 'soccer', 'in', 'the', 'open', 'field', 'until', 'sunset.'],
    ['He', 'carefully', 'painted', 'the', 'fence', 'white', 'before', 'the', 'storm', 'arrived.'],
    ['They', 'visited', 'the', 'museum', 'to', 'learn', 'about', 'ancient', 'civilizations.'],
    ['Maria', 'studies', 'biology', 'every', 'evening', 'after', 'dinner.'],
    ['The', 'cat', 'jumped', 'onto', 'the', 'windowsill', 'to', 'watch', 'the', 'birds.'],
    ['A', 'gentle', 'breeze', 'swept', 'through', 'the', 'tall', 'pine', 'trees.'],
    ['He', 'found', 'a', 'wallet', 'on', 'the', 'sidewalk', 'and', 'turned', 'it', 'in.'],
    ['The', 'concert', 'ended', 'with', 'a', 'spectacular', 'fireworks', 'show.'],
    ['We', 'met', 'at', 'the', 'coffee', 'shop', 'for', 'our', 'weekly', 'catch-up.'],
    ['The', 'train', 'arrived', 'five', 'minutes', 'ahead', 'of', 'schedule.'],
    ['She', 'smiled', 'as', 'she', 'opened', 'the', 'letter', 'from', 'her', 'grandmother.'],
    ['The', 'recipe', 'called', 'for', 'two', 'cups', 'of', 'flour', 'and', 'one', 'of', 'sugar.'],
    ['He', 'fixed', 'the', 'leaking', 'faucet', 'with', 'a', 'new', 'rubber', 'washer.'],
    ['The', 'students', 'studied', 'hard', 'for', 'their', 'final', 'exams.'],
    ['A', 'rainbow', 'appeared', 'after', 'the', 'heavy', 'rain', 'stopped.'],
    ['The', 'dog', 'barked', 'excitedly', 'when', 'the', 'mail', 'carrier', 'approached.'],
    ['I', 'lost', 'my', 'keys', 'somewhere', 'between', 'the', 'park', 'and', 'the', 'store.'],
    ['They', 'enjoyed', 'a', 'picnic', 'by', 'the', 'riverbank', 'last', 'weekend.'],
    ['The', 'author', 'signed', 'copies', 'of', 'her', 'new', 'book', 'at', 'the', 'event.'],
    ['She', 'taught', 'herself', 'to', 'play', 'the', 'piano', 'by', 'watching', 'videos.'],
    ['He', 'wore', 'a', 'blue', 'suit', 'and', 'red', 'tie', 'to', 'the', 'interview.'],
    ['We', 'planted', 'roses', 'and', 'tulips', 'in', 'the', 'front', 'garden.'],
    ['The', 'fog', 'lifted', 'slowly', 'revealing', 'the', 'city', 'skyline.'],
    ['She', 'made', 'a', 'promise', 'she', 'knew', 'she', 'would', 'keep.'],
    ['The', 'lighthouse', 'guided', 'the', 'ship', 'safely', 'through', 'the', 'fog.'],
    ['He', 'jogs', 'every', 'morning', 'before', 'work', 'to', 'stay', 'fit.'],
    ['The', 'twins', 'wore', 'matching', 'outfits', 'to', 'the', 'party.'],
    ['A', 'deer', 'crossed', 'the', 'road', 'as', 'we', 'drove', 'through', 'the', 'woods.'],
    ['The', 'fireworks', 'lit', 'up', 'the', 'night', 'sky', 'in', 'vibrant', 'colors.'],
    ['The', 'room', 'was', 'silent', 'except', 'for', 'the', 'ticking', 'clock.'],
    ['She', 'knitted', 'a', 'scarf', 'for', 'her', 'grandfather\'s', 'birthday.'],
    ['He', 'solved', 'the', 'puzzle', 'faster', 'than', 'anyone', 'else', 'in', 'the', 'room.'],
    ['The', 'birds', 'sang', 'loudly', 'in', 'the', 'early', 'morning', 'light.'],
    ['We', 'bought', 'tickets', 'to', 'see', 'the', 'new', 'action', 'movie.'],
    ['The', 'bakery', 'smelled', 'like', 'fresh', 'bread', 'and', 'cinnamon.'],
    ['He', 'spilled', 'coffee', 'on', 'his', 'notes', 'before', 'the', 'meeting', 'started.'],
    ['The', 'old', 'man', 'fed', 'the', 'pigeons', 'every', 'afternoon.'],
    ['She', 'practiced', 'yoga', 'to', 'relax', 'and', 'clear', 'her', 'mind.'],
    ['The', 'ice', 'cream', 'truck', 'played', 'a', 'cheerful', 'tune.'],
    ['I', 'watched', 'the', 'stars', 'until', 'I', 'fell', 'asleep', 'on', 'the', 'porch.'],
    ['They', 'built', 'a', 'snowman', 'after', 'the', 'first', 'snowfall', 'of', 'the', 'year.'],
    ['She', 'found', 'a', 'four-leaf', 'clover', 'in', 'the', 'grassy', 'meadow.'],
    ['The', 'baby', 'laughed', 'when', 'the', 'dog', 'licked', 'her', 'toes.'],
    ['He', 'read', 'every', 'book', 'in', 'the', 'library\'s', 'mystery', 'section.'],
    ['The', 'sunflowers', 'turned', 'to', 'face', 'the', 'morning', 'light.'],
    ['She', 'wore', 'her', 'favorite', 'dress', 'to', 'the', 'dance.'],
    ['The', 'artist', 'used', 'bold', 'colors', 'to', 'express', 'his', 'emotions.'],
    ['The', 'bus', 'stopped', 'suddenly', 'to', 'avoid', 'hitting', 'a', 'squirrel.'],
    ['The', 'waves', 'crashed', 'against', 'the', 'rocks', 'during', 'the', 'storm.'],
    ['She', 'whispered', 'a', 'secret', 'to', 'her', 'best', 'friend.'],
    ['The', 'hallway', 'echoed', 'with', 'the', 'sound', 'of', 'footsteps.'],
    ['He', 'won', 'a', 'gold', 'medal', 'in', 'the', 'swimming', 'competition.'],
    ['A', 'hummingbird', 'hovered', 'above', 'the', 'blooming', 'flowers.'],
    ['The', 'teacher', 'handed', 'out', 'the', 'test', 'results', 'with', 'a', 'smile.'],
    ['She', 'tied', 'her', 'shoelaces', 'tightly', 'before', 'the', 'race', 'began.'],
    ['We', 'watched', 'the', 'sunset', 'from', 'the', 'top', 'of', 'the', 'hill.'],
    ['He', 'carried', 'the', 'groceries', 'inside', 'while', 'it', 'was', 'still', 'raining.'],
    ['The', 'children', 'built', 'a', 'fort', 'using', 'blankets', 'and', 'pillows.'],
    ['She', 'listened', 'to', 'classical', 'music', 'while', 'painting.'],
    ['The', 'leaves', 'rustled', 'in', 'the', 'autumn', 'breeze.'],
    ['He', 'carved', 'their', 'initials', 'into', 'the', 'old', 'oak', 'tree.'],
    ['They', 'danced', 'together', 'under', 'the', 'stars', 'at', 'the', 'wedding.'],
    ['The', 'cake', 'was', 'decorated', 'with', 'fresh', 'strawberries', 'and', 'cream.'],
    ['I', 'wrote', 'a', 'letter', 'to', 'my', 'future', 'self', 'last', 'night.'],
    ['The', 'wind', 'howled', 'through', 'the', 'empty', 'alleyways.'],
    ['She', 'grew', 'tomatoes', 'and', 'cucumbers', 'in', 'her', 'backyard.'],
    ['The', 'sky', 'turned', 'pink', 'and', 'orange', 'at', 'dusk.'],
    ['He', 'carefully', 'placed', 'the', 'fragile', 'vase', 'on', 'the', 'shelf.'],
    ['The', 'baby', 'slept', 'peacefully', 'in', 'her', 'crib.'],
    ['We', 'cheered', 'when', 'our', 'team', 'scored', 'the', 'winning', 'goal.'],
    ['The', 'candle', 'flickered', 'as', 'the', 'door', 'opened.'],
    ['He', 'saved', 'every', 'penny', 'to', 'buy', 'a', 'new', 'bicycle.'],
    ['She', 'played', 'the', 'violin', 'beautifully', 'at', 'the', 'recital.'],
    ['A', 'butterfly', 'landed', 'gently', 'on', 'her', 'outstretched', 'hand.'],
    ['The', 'hikers', 'reached', 'the', 'summit', 'just', 'before', 'noon.'],
    ['The', 'soup', 'simmered', 'on', 'the', 'stove', 'filling', 'the', 'room', 'with', 'aroma.'],
    ['He', 'painted', 'a', 'landscape', 'inspired', 'by', 'his', 'childhood', 'farm.'],
    ['They', 'laughed', 'until', 'their', 'sides', 'hurt.'],
    ['She', 'looked', 'out', 'the', 'window', 'and', 'saw', 'the', 'first', 'snowflake', 'fall.'],
    ['The', 'movie', 'made', 'everyone', 'in', 'the', 'theater', 'cry.'],
    ['He', 'opened', 'the', 'dusty', 'attic', 'door', 'with', 'curiosity.'],
    ['The', 'team', 'trained', 'hard', 'for', 'the', 'upcoming', 'tournament.'],
    ['We', 'watched', 'as', 'the', 'hot', 'air', 'balloon', 'rose', 'into', 'the', 'sky.'],
    ['The', 'letter', 'arrived', 'exactly', 'one', 'year', 'after', 'it', 'was', 'sent.'],
    ['She', 'thanked', 'everyone', 'for', 'coming', 'to', 'her', 'graduation.'],
    ['The', 'clock', 'struck', 'midnight', 'as', 'the', 'fireworks', 'exploded.'],
    ['He', 'whistled', 'a', 'cheerful', 'tune', 'on', 'his', 'way', 'to', 'work.'],
    ['The', 'dog', 'wagged', 'its', 'tail', 'when', 'it', 'saw', 'its', 'owner.'],
    ['She', 'organized', 'her', 'books', 'by', 'genre', 'and', 'color.'],
    ['The', 'painting', 'hung', 'above', 'the', 'fireplace', 'in', 'a', 'gold', 'frame.'],
    ['The', 'old', 'piano', 'still', 'worked', 'despite', 'its', 'age.'],
    ['We', 'saw', 'dolphins', 'swimming', 'near', 'the', 'boat.'],
    ['The', 'garden', 'was', 'full', 'of', 'blooming', 'lavender', 'and', 'bees.'],
    ['He', 'learned', 'to', 'ride', 'a', 'bike', 'without', 'training', 'wheels.'],
    ['The', 'train', 'whistle', 'echoed', 'across', 'the', 'valley.'],
    ['She', 'wore', 'gloves', 'to', 'protect', 'her', 'hands', 'from', 'the', 'cold.'],
    ['The', 'fog', 'was', 'so', 'thick', 'we', 'could', 'barely', 'see', 'the', 'road.'],
    ['They', 'toasted', 'marshmallows', 'around', 'the', 'campfire.']
]

const solution = `

def concat_with_space(*strings):
    return ' '.join(strings)

`

new Assignment(
    "concat_with_space",
    () => {
        return sentences[randint(0, sentences.length-1)]
    },
    solution
)

</script>
