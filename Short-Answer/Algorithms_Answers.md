
Add your answers to the Algorithms exercises here.

## Exercise I
a) The `while` loop will run `n ** 3 / n ** 2 = n` times, so _O(n)_
b) The first three `for` loops in isolation have _O(n)_ time complexity, and the fourth has _O(c)_ time, since they are nested the overall time complexity would be _O(n^3)_
c) `bunnyEars` will run `bunnies` times (assuming `bunnies >= 0`) so the time complexity would be linear _O(n)_

## Exercise II
I would start by dropping the egg off of the top floor (_n_-th story). If the egg doesn't break you've found _f_. If the egg breaks try the story halfway between the _nth_ story and the ground (the _n/2_-th story, roughly), and if:
  a) the egg breaks from that height, you can rule out all stories **above** it and try dropping from the story as close to halfway between the current one and the ground (or the one closest to the ground that hasn't been ruled out)
  b) the egg doesn't break, you can rule out all stories **below** it and try dropping from the story as close to halfway between the current one and the top-floor (or the one closest to the top-floor that hasn't been ruled out)
You can repeat this process, eliminating close to half the possible candidates for _f_ each time, so the time complexity would be _O(log n)_.