# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Phillip Che**

Time spent: **4** hours spent in total

Link to project: https://glitch.com/edit/#!/quilted-exciting-wheel

## Required Functionality

The following **required** functionality is complete:

* [ ] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [ ] "Start" button toggles between "Start" and "Stop" when clicked. 
* [ ] Game buttons each light up and play a sound when clicked. 
* [ ] Computer plays back sequence of clues including sound and visual cue for each button
* [ ] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [ ] User wins the game after guessing a complete pattern
* [ ] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ ] Player only loses after 3 mistakes (instead of on the first mistake)

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![](https://i.imgur.com/lBItb7V.gif)
![](https://i.imgur.com/IZaF2jO.gif)
![](https://i.imgur.com/Uex2aSD.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

The only outside resource I used was this website which I found on the prework steps: https://www.w3schools.com/css/.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

The main challenge which I encountered in this mini-project occurred in the implementation of the guess() method. At first, I had trouble understanding what exactly the end of a turn meant in the flow chart. For instance, if the end of a turn meant after the user clicked each individual button, or after the user has clicked all the correct buttons in a sequence with respect to their progress. Due to my confusion, I initially implemented a for loop which would iterate through each button up to the user’s progress, checking each time that the user pressed the button if it was equal to the corresponding button in pattern[progress]. I quickly realized that the for loop was unnecessary since the guess() method only passes one button to check, meaning that the game would end as soon as the button passed did not equal to the one in pattern[progress]. After removing the for loop, however, I found another issue that sometimes resulted in ending the game even when I would click the correct button. This issue would occur after the second iteration when the number in the pattern array was not equal to the number before. This was due to the fact that I had the check between the user that the button clicked, and the button corresponding to pattern[progress] which meant that the button was always comparing itself to the latest button in the sequence on every turn instead of restarting from the beginning. I fixed this issue by changing pattern[progress] to pattern[guessCounter] since I looked back at the code and recalled that the guessCounter global variable was set back to 0 each time the playClueSequence() method was called. The entire game functioned properly after that.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

After completing my prework submission, I am most curious about how exactly the javascript or .js files work with the .html files in regards to web development as well as the capabilities and methods between them. Specifically, while working on adding the optional feature of having three strikes before losing the game, I wanted to display the amount of tries left the user had under the buttons, however, I was unsure how to exactly display the javascript variable, mistakes, on the page in the .html file. Instead, I simply sent out an alert displaying how many tries the user had left each time they clicked the wrong button. Additionally, I would like to learn more about how to extract certain elements on a webpage in order to utilize them in javascript methods as well as implementing animations to the page.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

There are many aspects of the game which can be improved on, however, if I had a few more hours to work on this project, I would most definitely be prioritizing the design to the page to be more appealing to the user such as changing the colors, adding more texture and text to the background as well as some animations to give it life. I would also spend my remaining time on the interactions and system feedback between the game and the user to make it more enjoyable. Other optional features I would like to work on include difficulty levels with corresponding leaderboards as well as adding game modes such as having a timer, no extra lives, no color option, and no sound option. 

## Interview Recording URL Link

[My 5-minute Interview Recording](https://drive.google.com/file/d/1Y6GkZjW81a_nUyvTWmOb0T-pe2qzHs0p/view)


## License

    Copyright Phillip Che

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.