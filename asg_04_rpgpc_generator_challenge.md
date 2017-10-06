# Problem Set 04: The Tyranny of Choice

## Role Playing Game Player Character (RPG PC) Generator Challenge

_Great. Strength 3. I can barely draw a breath, let alone a sword._

---

_So I was playing [D&D](http://dnd.wizards.com/dungeons-and-dragons/what-is-dd) last week, 'cause yeah, some stereotypes are totally justified._

_We were just starting a new campaign, so it was time to roll up a new character._

_I think you can see where this is going._

_You're going to make a tool that takes in 4 numbers (i.e. "dice rolls") and a race, and calculates the dexterity score and dexterity modifier for the character based on those rolls. Don’t worry, if you’ve never played D&D, I know this will likely sound like a foreign language to you, so there is a quick primer on this comin’ up…_

---

**SOME BACKGROUND (you can skip this if you already speak RPG)**

So D&D (or Dungeons and Dragons) is an example of a _Role Playing Game_, or _RPG_. To put it very simply, in an RPG, you pretend you're someone else (like a character out of a fantasy novel, or science fiction movie, etc.) and you have some sort of adventure with a number of like-minded people. There are usually some (and by some, I mean way too many) rules involved. And dice - often oddly-shaped ones. And there's usually snacking involved.

Anyway, in D&D, when you want to start an adventure, you have to create your _character_. In the current basic version of D&D, your character can be one of four races:
* human (no surprises here)
* dwarf (think Gimli from the Lord of the Rings movies)
* elf (think Legolas from the same movie)
* halfling (think one of the hobbits from...the same movie)

While you're creating your character, you'll also need to determine his or her _abilitiy scores_ - things like how strong she is, how smart, how nimble, etc. To do this in D&D, you roll some dice, add up the numbers, and write that sum down on a sheet for later reference. 

Your might get to add a small number to your dice sum based on your race as well.

The number you get for each ability score will determine its _ability modifier_. If you roll a high sum, you'll get a positive modifier ranging from +1 to +4. If you roll a low sum, you'll get a negative modifier ranging from -1 to -4. You use these modifiers over the course of the game, so they're kinda important. Look at the the _Ability Scores and Modifiers_ table on page 7 of the  [D&D Player's Basic Rules](http://media.wizards.com/2016/downloads/DND/PlayerBasicRulesV03.pdf) to see how the ability scores and ability modifiers are related. 

For this challenge, we'll deal with the **dexterity** ability - it represents how nimble your character is. A character with high dexterity can dodge things (like arrows or swords being swung at their head), can run across a tightrope like a freaking cat, and are great at hitting things with bows and the like.

That's all the background you need to know for this assignment.

**MAKE THIS HAPPEN:**

1. Ask the user to enter in their 4 "rolls". Assume they will enter in 4 numbers from 1 to 6. You need to sum up *the highest 3 of those numbers*. 
    * Ex. If the numbers were 3 2 5 5, you would sum up 3, 5, and 5 for a total of 13.
    * You can have these numbers entered one at a time, or all on the same line with tabs or spaces between.
1. Ask the user for which _race_ they wish to be - this choice might affect the dexterity sum rolled earlier. To keep things simple, we will ignore subraces (sorry, fans), so here are the only choices you have to worry about, along with the change to the dexterity sum:
    * user enters M or m => **human** => add 1 to the dexterity sum
    * user enters D or d => **dwarf** => no change in dexterity sum
    * user enters E or e => **elf** => add 2 to the dexterity sum
    * user enters H or h => **halfling** => add 2 to the dexterity sum
1. Print to the console the following information in this order (you can format it how you like):
    * Race
    * Dexterity score; if it has been modified by the race, it should have an asterisk next to it.
    * Dexterity modifier. (ranging from -3 to +3, and yes, you have to add the  + or - sign)
    * If the dexterity score _was_ modified by the class, an additional note must be displayed stating the size of the racial increase.
        * The note must be worded exactly like this:  
             `Note: applied racial modifier (+1)`

Output Example:

Let's assume the user has entered the rolls 1,4,1,6 and a race of halfling. Taking the highest 3 numbers (1,4,6), we have a dexterity sum of 11. But because the race was halfling, we add 2 to this sum to get 13. The table on page 7 of the manual says that gives a modifier of +1. So an acceptable output would be:

`Race: Halfling`  
`Dexterity: 13*`  
`Modifier: +1`  
`Note: applied racial modifier (+2)`


**NOTES:**

* You _may_ use an enum (see special topic 3.4 in the text, or do some research) for the races if you wish. Using - or not using - enums will not affect your mark in any way!
* You **can** assume they will enter in a valid letter (ex. "D" for dwarf)...but you **can't** assume they will enter in a **capital** letter.
* Hint: there is a mathematical way to determine the ability modifier from the ability score.

