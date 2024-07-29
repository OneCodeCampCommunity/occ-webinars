```js
// Array of question objects
const questions = [
  {
    question: "What does 'HTML' stand for?",
    options: [
      "Hyper Text Markup Language",
      "High Technology Modern Language",
      "Home Tool Markup Language",
      "Hyperlink and Text Markup Language"
    ],
    correctAnswer: 0
  },
  {
    question:
      "Which element is used to link an external CSS file to an HTML document?",
    options: ["<style>", "<link>", "<css>", "<stylesheet>"],
    correctAnswer: 1
  },
  {
    question:
      "In JavaScript, which function is used to print text to the console?",
    options: ["console.log()", "print()", "log()", "write()"],
    correctAnswer: 0
  },
  {
    question:
      "What is the correct CSS property to change the background color?",
    options: ["bgcolor", "background-color", "bg-color", "color-background"],
    correctAnswer: 1
  },
  {
    question: "Which HTML tag is used to define an ordered list?",
    options: ["<ul>", "<li>", "<dl>", "<ol>"],
    correctAnswer: 3
  },
  {
    question: "Which operator is used to concatenate strings in JavaScript?",
    options: ["&", "+", "++", "="],
    correctAnswer: 1
  },
  {
    question:
      "Which CSS property is used to control the spacing between lines of text?",
    options: ["line-height", "font-size", "text-spacing", "line-spacing"],
    correctAnswer: 0
  },
  {
    question: "In JavaScript, how do you declare a variable?",
    options: ["new", "var", "variable", "let"],
    correctAnswer: 1
  },
  {
    question: "Which HTML tag is used to create a hyperlink?",
    options: ["<link>", "<a>", "<href>", "<hyperlink>"],
    correctAnswer: 1
  },
  {
    question: "Which CSS property is used to make text bold?",
    options: ["font-style", "text-weight", "font-weight", "bold"],
    correctAnswer: 2
  }
];

// Variables to track current question index and user's score
let currentQuestion = 0;
let score = 0;

// DOM elements
const questionElement = document.getElementById("question");
const optionsElement = document.getElementById("options");
const scoreElement = document.getElementById("score");
const retryButton = document.getElementById("retry-btn");

// Display the current question and options
function showQuestion() {
  const question = questions[currentQuestion];
  questionElement.textContent = question.question;

  // Clear previous options
  optionsElement.innerHTML = "";

  // Create buttons for each option and attach click event listeners
  question.options.forEach((option, index) => {
    const button = document.createElement("button");
    button.textContent = option;
    button.addEventListener("click", () => checkAnswer(index));
    optionsElement.appendChild(button);
  });
}

// Check the selected answer and update score
function checkAnswer(selectedIndex) {
  const question = questions[currentQuestion];
  if (selectedIndex === question.correctAnswer) {
    score++;
  }

  // Move to the next question
  currentQuestion++;

  // Show the next question or the final result
  if (currentQuestion < questions.length) {
    showQuestion();
  } else {
    showResult();
  }
}

// Display the final result
function showResult() {
  questionElement.textContent = "Quiz Complete!";
  optionsElement.style.display = "none";
  scoreElement.textContent = `Your Score: ${score}/${questions.length}`;
  retryButton.style.display = "block";
  scoreElement.style.display = "block";
}

// Reset the quiz to start over
function resetQuiz() {
  currentQuestion = 0;
  score = 0;
  optionsElement.style.display = "block";
  retryButton.style.display = "none";
  showQuestion();
  scoreElement.style.display = "none";
}

// Attach event listener to the retry button
retryButton.addEventListener("click", () => resetQuiz());

// Initialize the quiz by showing the first question
showQuestion();
```