# Problem Set 04: The Tyranny of Choice

## Car AI Challenge

_It was my car's fault._

---

_Saw a pretty cool [TED talk video](https://youtu.be/ixIoDYVfKA0) about self-driving vehicles.  It was thought-provoking. Thought I'd pass that provocation on to you._

_After watching the TED video, I dug around a bit and found [this site](http://moralmachine.mit.edu/), which provides the basis for this challenge._

_Let's assume that the brakes have failed on a (nearly) fully autonomous self-driving car carrying a given number of adult and child passengers. In front of the car, there is a crosswalk with a given number of adult and child pedestrians crossing. To the left of the car is a very solid concrete barrier._

_The car needs to make a decision: veer to the left, ploughing into the barrier, killing the car's passengers, or continue going straight, killing the pedestrians in the crosswalk. Pretty grim stuff._

_We will evaluate the situation in a very simple manner: assign a base point value for each adult life and each child life and add up the points in the two groups: whichever group has the most points "wins" (i.e. lives). If the two scores are within a given threshold of each other, we will call this a **tough call** and have the car decide which group lives and dies via user input._

---

**MAKE THIS HAPPEN:**

1. Prompt the user for, and read in, the number of adults in the car.
1. Prompt the user for, and read in, the number of children in the car.
1. Prompt the user for, and read in, the number of adults in the crosswalk.
1. Prompt the user for, and read in, the number of children in the crosswalk.
1. Ask the user whether the lives of the car's occupants should be valued over the lives of the pedestrians in case of a **tough call**.
    * You can assume the user will enter in a 'y' or 'n', but can't be sure of the case of the letter.
1. Output a fatality report, consisiting of the following, in order:
    1. The group killed (PEDESTRIANS or OCCUPANTS)
    1. The number of adults killed.
    1. The number of children killed.



**NOTES:**
* You can assume that adult lives are worth **100 points** and that child lives are worth **145 points**.
* The threshold for a **tough call** is **10 points or less** .
* You _may_ use an enum (see special topic 3.4 in the text, or do some research) for the two groups (passenger and pedestrian) if you wish. Using - or not using - enums will not affect your mark in any way!
