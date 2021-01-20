# Add prerequisites to practice exercises

Exercism V3 introduces a new type of exercise: [Concept Exercises](https://github.com/exercism/v3-docs/blob/master/product/concept-exercises.md). All existing (V2) exercises will become [Practice Exercises](https://github.com/exercism/v3-docs/blob/master/product/practice-exercises.md).

Concept Exercises and Practice Exercises are linked to each other via [Concepts](https://github.com/exercism/v3-docs/blob/master/anatomy/tracks/concepts.md). Concepts are taught by Concept Exercises and practiced in Practice Exercises. Each Exercise (Concept or Practice) has prerequisites, which must be met to unlock an Exercise -  once all the prerequisite Concepts have been "taught" by a Concept Exercise, the exercise itself becomes unlocked.

For example, in some languages completing the Concept Exercises that teach "String Interpolation"  and "Optional Parameters" might then unlock `two-fer`.


Each Exercise should have one or more prerequisites, where each prerequisite describes the minimal set of concepts the Practice Exercise requires the student to be familiar with. The only exception is a single initial Concept Exercise (normally targeting the `basics` Concept)


Although ideally all Concepts should be taught by Concept Exercises, we recognise that it will take time for tracks to achieve that. Any Practice Exercises that have prerequisites, which are not taught by Concept Exercises, will become unlocked once the final Concept Exercise has been completed.


## Tracking

https://github.com/exercism/v3-launch/issues/6
