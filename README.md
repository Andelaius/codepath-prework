# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Andreas Miller**

Time spent: **5** hours spent in total

Link to project: (https://glitch.com/~achieved-night-tub)

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [x] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![x](http://g.recordit.co/zmXQbJaMjr.gif)
![x](http://g.recordit.co/lI4Nww6W9C.gif)
![x](http://g.recordit.co/E8wolQpctb.gif)
![x](http://g.recordit.co/19np4VCt1v.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.
 
   Websites:
      https://www.w3schools.com/jsref/met_win_setinterval.asp
      https://developer.mozilla.org/en-US/docs/web/javascript/reference/global_objects/math/random
      https://www.w3schools.com/colors/colors_names.asp

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

    By far the biggest challenge I encountered in creating this submission was implementing the sixth optional feature: the ticking timer. I wasn’t initially sure how I would do this, so I took the given hint and looked into the setInterval and clearInterval functions on the W3Schools website. After getting accustomed to what those functions do, I also looked at a couple of examples that W3Schools had. The tricky thing there was that the examples were given in HTML, so I was under the impression that I would be able to do the same with this project.
	  After a little while, I had successfully created the timer in HTML, but soon realized that I couldn’t control when I wanted it to start or stop; it initialized at 10 but then continuously dropped to increasingly negative numbers. From there, I recognized that I would have to implement the timer in JavaScript. Luckily, the basic structure of what I had already written carried over nicely, so I didn’t have to completely restart. 
	  When I was creating the start and stop methods for the timer, I encountered another problem, this time with my ‘clock’ variable, which implements the setInterval function. Originally, I declared it in my startTimer function, which of course meant that my stopTimer function couldn’t access it and stop it. This was a big dilemma for me because I knew I needed to declare ‘clock’ as a global variable, but doing so would make it start as soon as the game started, resulting in calling the noTime function (which ends the game when called) every time 10sec had passed in a game. At that point, the game was virtually unplayable. 
    It took a lot of time for me to brainstorm how fix this, during which I kept referring to W3Schools to figure out how I could manipulate the setInterval function. At some point I had an “aha!” moment when I realized I could insert a parameter (‘key’) that would require a specific argument (‘in’) to run the noTime function. Modifying my code to reflect this, I finally got my timer to functionally work how it was intended to.


3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

    I have a lot of questions about web development, especially on the macroscale. In fact, most of my curiosity revolves around the execution of web development at the industry level. For example, what is the planning process for creating a product and how does one balance planning and implementing? Do teams effectively code together or are individuals in a team responsible for subparts of the project? Is there a way to meaningfully measure progress on a product? What does a successful day look like?
    I feel like producing code at the company level can be very tricky as just about everything has to be communicated and understood, not to mention the time constraints. With small, individual projects it’s relatively easy to keep track of everything in your head, know the ins and outs of the entire project, and work on it whenever preferred. That obviously isn’t possible with more demanding projects, so in general, I want to know how that is all done. 


4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

    If I had more time to work on this project, I would fix and add additional features. I would first focus my efforts on the placement of my startTimer function. For some reason that I could not ascertain, the current placement of that function (right after the for loop in the playClueSequence) starts the timer at the same time that a clue is just starting to be given. This results in the player not actually having 10 seconds to repeat the clue. That spot in the code seemed like the most logical place to begin the timer, but I must be missing/misunderstanding something about the functionality of the playClueSequence.
    Also, I would seek to spruce up the buttons by adding images and audio to them. There are so many different ways that this could be done and I would definitely have a fun time personalizing the game in this way. I think this would also help make the game more interactive and fun to play.




## Interview Recording URL Link

[My 5-minute Interview Recording](https://youtu.be/RX3tq8j1xyc)


## License

    Copyright Andreas Miller

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
