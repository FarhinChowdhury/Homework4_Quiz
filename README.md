# Homework4_Quiz
What I need to do:
AS A coding bootcamp student
I WANT to take a timed quiz on JavaScript fundamentals that stores high scores
SO THAT I can gauge my progress compared to my peers

To Do List:
GIVEN I am taking a code quiz
WHEN I click the start button
THEN a timer starts and I am presented with a question
WHEN I answer a question
THEN I am presented with another question
WHEN I answer a question incorrectly
THEN time is subtracted from the clock
WHEN all questions are answered or the timer reaches 0
THEN the game is over
WHEN the game is over
THEN I can save my initials and score

My Process:
1. I started of by creating the basic html for my quiz what I needed:
    - A starting page with Title, instructions, a start button and also a nav bar that would indicate the score and time.
    - I used boot straps for the nav bar and the start button, also for the score and time I put them under a card so it would be easier to indicate them with an id and also float them on opposite ends. 

2. I then went on creating my question container which included the same nav bar but showed the question and options which again were acquired from bootstraps, four button options for each quesion.

3. Finally for my html I had to create a score board which was simply a in a div container with the heading Score board and and the place for where the name and the score of the user will be placed.

4. for my css I kept it quite clean and simple wih the navbar being a yellow collor and the background white. with the option button being yellow. I made sure that the questions container and the score board page were both under the "hide" class. this will allow the css .hide{ display:none} to hide these contents and will appear when necessary as directed by the js code

5. For my java code I started with declaring some global variables for example:
    - var score = 0 //for the starting score to be 0 and once the user has a correct answer it will go up by 1.
    - var timer = 60// this is the total time that the user has
    - var questions = ["an object with all the qestion, answer and correctanswer"]// array of objects for each question.
    - var correctAnswer // for when the answer of the user matches the actual answer of the question as displaed in the questions variable.

6. afterwards I wrote my first function called startingQuiz() this function is linked with click event for when the start button is pressed on line(187). Thus once the strat button is clicked the starting page code will hide and the question container code will appear.

7. The next function was the showQuestion() this function uses DOM delegation to populate the question and option buttons witht the objects in the question arrays. this question was then called on in startingQuiz.

8. Then I worked on the decreaseTimer() function which again uses dom delegation to populate the time card and creates a timer that decreases by 1 every second. This function was also called on the startingQuiz function so that once the start button was pressed the timer starts.

9. The next funtion called nextQuestion() which helps jump to the next question once a question is answered. this is also linked to an eventlistener 'click on line 188. This function passes thorugh event to compare the event target value with the correct answer. Thus is it does not match 10 seconds of the time is deducted and goes on to the next question but if it does match 1 point is added to the score. 

10. Lastly the last function is called ScorePage() which hides the question container and shows the scoreboard page from the html. so once all the questions are answered by haveing the questionCounter== questions.length OR the timer is 0. the timer is stoped and the a prompt appears. in the prompt the user is asked for their name and then the score board appears with the user's name and score. 
