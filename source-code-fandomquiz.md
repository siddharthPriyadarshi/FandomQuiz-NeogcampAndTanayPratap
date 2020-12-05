# Source Code
***

```
var readlineSync = require("readline-sync");
const chalk = require('chalk');

var userName = readlineSync.question(chalk.bold("Enter your name: "));

console.log("\nWelcome ",chalk.red.italic(userName)," to my Quiz "+"\nTopic: Quiz on NEOGCAMP and TANAY PRATAP");

console.log(chalk.red("Rules:")+chalk.magenta.italic("\n1. There are 7 questions.\n2. 1 point will be rewarded for every correct answer\n3. No minus marking\n4. Write ans in lower case\n5. Use valid credentials\n"));

console.log(chalk.green.underline.bold("Lets! Play :-))"));
var score = 0; //default value of score
var highestScore=2;

var questions=[ {
  question: chalk.bold("\n1. Who is the mentor of ongoing neogcamp Youtube Tutorials?\n")+chalk.blue("A. Tanay Pratap \nB. Hitesh Choudhry \nC. Sundar Pichai\nD. Mark Zuckerberg\n")+"Answer: ",
  answer:"A"
},
{
  question: chalk.bold("2. In which company Tanay Pratap works? \n")+chalk.blue("A. Google \nB. Oracle \nC. Microsoft\nD. Adobe\n")+"Answer:",
  answer: "C"
},
{
  question: chalk.bold("3. Who can opt for the ongoing neog-camp tutorials ?\n")+chalk.blue("A. Professionals only \nB. Any Beginner\nC. Industries Experts\nD. None of these\n")+"Answer:",
  answer:"B"
},
{
  question: chalk.bold("4. In which platform learners have to submit their projects ?")+ chalk.blue("\nA. Google Classrooms \nB. Facebook Page \nC. In Discord Server\nD. Gmail\n")+"Answer:",
  answer: "C"
},
{
  question: chalk.bold("5. How neog camp will help an individual ?")+chalk.blue("\nA. It will help to increase vocabulary \nB. Train individual to get a Job \nC. Enhance Mathematical Concepts \nD. To score good marks in Exams \n")+"Answer:",
  answer: "B"
},
{
  question: chalk.bold("6. What kind of camp is neoG camp ?")+chalk.blue("\nA. Gaming Bootcamp \nB. Debating Bootcamp \nC. Web Development Bootcamp \nD. Both A and B\n")+"Answer:",
  answer: "computer"
},
{
  question: chalk.bold("7. Is level 0 paid or free ?")+chalk.blue("\nA. Yes, absoulely free \nB. No,its vetry costly \nC. Can't say \nD. None of the above\n")+"Answer:",
  answer: "A"
}]

for(var i=0; i<questions.length; i++) {
  var userAns = readlineSync.question(questions[i].question)
  if (userAns === questions[i].answer) {
    score = score +1;
    console.log("You are"+chalk.green(" right!")+"\nYour score: ",score);
    console.log();
  }
  else {
    console.log(chalk.red("You are"+chalk.red(" wrong!")));
    console.log();
  }
}

console.log("\nThanks for playing\n\nYour final score: ",score);
if (score > highestScore) {
  console.log(chalk.yellow.bold("Congratulations!")+" You have beaten the highest scorer.")
}
console.log("Hihgest Score   :",highestScore);

console.log(chalk.red("\n** If you have beaten the highest score then dm the screenshot to let it update!"));

```
