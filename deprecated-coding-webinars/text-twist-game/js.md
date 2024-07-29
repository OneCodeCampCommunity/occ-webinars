```javascript
const words = [
  "programming",
  "developer",
  "javascript",
  "algorithm",
  "variable",
  "function",
  "debugging",
  "syntax",
  "loop",
  "database"
];

let currentWordIndex = 0;
let score = 0;

function shuffleText(text) {
  const textArray = text.split("");
  for (let i = textArray.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [textArray[i], textArray[j]] = [textArray[j], textArray[i]];
  }
  return textArray;
}

function displayWords() {
  const wordContainer = document.getElementById("word-container");
  for (let i = 0; i < words.length; i++) {
    const wordBox = document.createElement("div");
    wordBox.className = "word-box";
    const shuffledLetters = shuffleText(words[i]);
    for (let j = 0; j < shuffledLetters.length; j++) {
      const letterBox = document.createElement("div");
      letterBox.className = "letter-box";
      letterBox.textContent = "";
      wordBox.appendChild(letterBox);
    }
    wordContainer.appendChild(wordBox);
  }
}

function revealWord() {
  const wordContainer = document.getElementById("word-container");
  const wordBoxes = wordContainer.querySelectorAll(".word-box");
  const wordToReveal = words[currentWordIndex];

  // Clear the current content of the word box
  wordBoxes[currentWordIndex].innerHTML = "";

  // Create letter boxes for each character of the word
  for (let i = 0; i < wordToReveal.length; i++) {
    const letterBox = document.createElement("div");
    letterBox.className = "letter-box";
    letterBox.textContent = wordToReveal[i];
    wordBoxes[currentWordIndex].appendChild(letterBox);
  }
}

function nextWord() {
  if (currentWordIndex < words.length) {
    const wordToGuess = document.getElementById("word-to-guess");
    wordToGuess.innerHTML = ""; // Clear the previous content

    const shuffledLetters = shuffleText(words[currentWordIndex]);
    for (let j = 0; j < shuffledLetters.length; j++) {
      const letterBox = document.createElement("div");
      letterBox.className = "letter-box";
      letterBox.textContent = shuffledLetters[j];
      wordToGuess.appendChild(letterBox);
    }
  } else {
    alert("Game Over! Your final score is: " + score);
  }
}

function checkAnswer() {
  const userInput = document.getElementById("user-input").value.toLowerCase();
  const word = words[currentWordIndex];
  if (userInput === word) {
    score++;
    document.getElementById("score").textContent = "Score: " + score;
    revealWord();
    currentWordIndex++;
    nextWord();
    document.getElementById("result-message").textContent = "Correct!";
  } else {
    document.getElementById("result-message").textContent = "Try again!";
  }
  document.getElementById("user-input").value = "";
}

displayWords();
nextWord();

document.getElementById("check-button").addEventListener("click", checkAnswer);
```