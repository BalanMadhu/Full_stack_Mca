# Full_stack_Mca
import React, { useState } from "react";
const allQuestions = {
  java: [
    {
      questionText: "What is the size of int in Java?",
      answerOptions: [
        { answerText: "16 bit", isCorrect: false },
        { answerText: "32 bit", isCorrect: true },
        { answerText: "64 bit", isCorrect: false },
        { answerText: "8 bit", isCorrect: false },
      ],
    },
    {
      questionText: "Which of these is not a Java feature?",
      answerOptions: [
        { answerText: "Object-oriented", isCorrect: false },
        { answerText: "Use of pointers", isCorrect: true },
        { answerText: "Portable", isCorrect: false },
        { answerText: "Dynamic", isCorrect: false },
      ],
    },
    {
      questionText: "Which keyword is used to inherit a class in Java?",
      answerOptions: [
        { answerText: "this", isCorrect: false },
        { answerText: "super", isCorrect: false },
        { answerText: "extends", isCorrect: true },
        { answerText: "implements", isCorrect: false },
      ],
    },
    {
      questionText: "Which of the following is not a primitive data type in Java?",
      answerOptions: [
        { answerText: "int", isCorrect: false },
        { answerText: "float", isCorrect: false },
        { answerText: "String", isCorrect: true },
        { answerText: "boolean", isCorrect: false },
      ],
    },
    {
      questionText: "What is the default value of a boolean variable in Java?",
      answerOptions: [
        { answerText: "true", isCorrect: false },
        { answerText: "false", isCorrect: true },
        { answerText: "0", isCorrect: false },
        { answerText: "null", isCorrect: false },
      ],
    },
    {
      questionText: "Which method is the entry point for a Java program?",
      answerOptions: [
        { answerText: "main()", isCorrect: true },
        { answerText: "start()", isCorrect: false },
        { answerText: "run()", isCorrect: false },
        { answerText: "init()", isCorrect: false },
      ],
    },
    {
      questionText: "Which exception is thrown when a null reference is accessed?",
      answerOptions: [
        { answerText: "ArrayIndexOutOfBoundsException", isCorrect: false },
        { answerText: "NullPointerException", isCorrect: true },
        { answerText: "IllegalArgumentException", isCorrect: false },
        { answerText: "ClassCastException", isCorrect: false },
      ],
    },
    {
      questionText: "Which keyword is used to define a constant variable in Java?",
      answerOptions: [
        { answerText: "static", isCorrect: false },
        { answerText: "final", isCorrect: true },
        { answerText: "const", isCorrect: false },
        { answerText: "immutable", isCorrect: false },
      ],
    },
    {
      questionText: "Which collection class allows you to grow or shrink its size dynamically?",
      answerOptions: [
        { answerText: "Array", isCorrect: false },
        { answerText: "ArrayList", isCorrect: true },
        { answerText: "LinkedList", isCorrect: true },
        { answerText: "HashMap", isCorrect: false },
      ],
    },
    {
      questionText: "Which keyword is used to handle exceptions in Java?",
      answerOptions: [
        { answerText: "try-catch", isCorrect: true },
        { answerText: "throw-catch", isCorrect: false },
        { answerText: "do-catch", isCorrect: false },
        { answerText: "handle-catch", isCorrect: false },
      ],
    },
  ],

  fullstack: [
    {
      questionText: "Which technology is used for frontend development?",
      answerOptions: [
        { answerText: "Node.js", isCorrect: false },
        { answerText: "React", isCorrect: true },
        { answerText: "Express", isCorrect: false },
        { answerText: "MongoDB", isCorrect: false },
      ],
    },
    {
      questionText: "Which database is NoSQL?",
      answerOptions: [
        { answerText: "MySQL", isCorrect: false },
        { answerText: "MongoDB", isCorrect: true },
        { answerText: "PostgreSQL", isCorrect: false },
        { answerText: "Oracle", isCorrect: false },
      ],
    },
    {
      questionText: "What does REST stand for?",
      answerOptions: [
        { answerText: "Representational State Transfer", isCorrect: true },
        { answerText: "Random State Transfer", isCorrect: false },
        { answerText: "Rapid State Transfer", isCorrect: false },
        { answerText: "None of these", isCorrect: false },
      ],
    },
    {
      questionText: "Which HTTP method is used to update a resource?",
      answerOptions: [
        { answerText: "GET", isCorrect: false },
        { answerText: "POST", isCorrect: false },
        { answerText: "PUT", isCorrect: true },
        { answerText: "DELETE", isCorrect: false },
      ],
    },
    {
      questionText: "Which tool is used for version control?",
      answerOptions: [
        { answerText: "Git", isCorrect: true },
        { answerText: "Webpack", isCorrect: false },
        { answerText: "Jenkins", isCorrect: false },
        { answerText: "Docker", isCorrect: false },
      ],
    },
    {
      questionText: "Which CSS framework is popular for responsive design?",
      answerOptions: [
        { answerText: "Bootstrap", isCorrect: true },
        { answerText: "Sass", isCorrect: false },
        { answerText: "Less", isCorrect: false },
        { answerText: "Styled Components", isCorrect: false },
      ],
    },
    {
      questionText: "Which backend framework is built on Node.js?",
      answerOptions: [
        { answerText: "Django", isCorrect: false },
        { answerText: "Flask", isCorrect: false },
        { answerText: "Express", isCorrect: true },
        { answerText: "Laravel", isCorrect: false },
      ],
    },
    {
      questionText: "Which of these is NOT a JavaScript framework?",
      answerOptions: [
        { answerText: "React", isCorrect: false },
        { answerText: "Angular", isCorrect: false },
        { answerText: "Vue", isCorrect: false },
        { answerText: "Laravel", isCorrect: true },
      ],
    },
    {
      questionText: "What language is primarily used for styling web pages?",
      answerOptions: [
        { answerText: "HTML", isCorrect: false },
        { answerText: "JavaScript", isCorrect: false },
        { answerText: "CSS", isCorrect: true },
        { answerText: "SQL", isCorrect: false },
      ],
    },
    {
      questionText: "What does JSON stand for?",
      answerOptions: [
        { answerText: "JavaScript Object Notation", isCorrect: true },
        { answerText: "Java Source Open Network", isCorrect: false },
        { answerText: "JavaScript Open Native", isCorrect: false },
        { answerText: "Java Source Object Notation", isCorrect: false },
      ],
    },
  ],

  machinelearning: [
    {
      questionText: "Which algorithm is used for classification problems?",
      answerOptions: [
        { answerText: "Linear Regression", isCorrect: false },
        { answerText: "Logistic Regression", isCorrect: true },
        { answerText: "K-Means", isCorrect: false },
        { answerText: "PCA", isCorrect: false },
      ],
    },
    {
      questionText: "What does overfitting mean?",
      answerOptions: [
        { answerText: "Model performs well on test data", isCorrect: false },
        { answerText: "Model performs well on training data but poorly on test data", isCorrect: true },
        { answerText: "Model performs poorly on all data", isCorrect: false },
        { answerText: "Model is undertrained", isCorrect: false },
      ],
    },
    {
      questionText: "Which technique is used to reduce dimensionality?",
      answerOptions: [
        { answerText: "Decision Tree", isCorrect: false },
        { answerText: "PCA", isCorrect: true },
        { answerText: "Random Forest", isCorrect: false },
        { answerText: "SVM", isCorrect: false },
      ],
    },
    {
      questionText: "What is the primary goal of unsupervised learning?",
      answerOptions: [
        { answerText: "Predict labels for data", isCorrect: false },
        { answerText: "Find hidden patterns in data", isCorrect: true },
        { answerText: "Improve supervised models", isCorrect: false },
        { answerText: "Label data manually", isCorrect: false },
      ],
    },
    {
      questionText: "Which evaluation metric is used for classification?",
      answerOptions: [
        { answerText: "Mean Squared Error", isCorrect: false },
        { answerText: "Accuracy", isCorrect: true },
        { answerText: "R-Squared", isCorrect: false },
        { answerText: "Sum of Squares", isCorrect: false },
      ],
    },
    {
      questionText: "Which algorithm is best suited for clustering?",
      answerOptions: [
        { answerText: "K-Nearest Neighbors", isCorrect: false },
        { answerText: "K-Means", isCorrect: true },
        { answerText: "Decision Tree", isCorrect: false },
        { answerText: "Naive Bayes", isCorrect: false },
      ],
    },
    {
      questionText: "What is the purpose of a confusion matrix?",
      answerOptions: [
        { answerText: "Visualize data distributions", isCorrect: false },
        { answerText: "Summarize classification performance", isCorrect: true },
        { answerText: "Show regression errors", isCorrect: false },
        { answerText: "Represent neural network layers", isCorrect: false },
      ],
    },
    {
      questionText: "Which of the following is a deep learning framework?",
      answerOptions: [
        { answerText: "TensorFlow", isCorrect: true },
        { answerText: "Scikit-learn", isCorrect: false },
        { answerText: "Pandas", isCorrect: false },
        { answerText: "NumPy", isCorrect: false },
      ],
    },
    {
      questionText: "Which technique helps to prevent overfitting?",
      answerOptions: [
        { answerText: "Increasing model complexity", isCorrect: false },
        { answerText: "Dropout", isCorrect: true },
        { answerText: "Ignoring validation data", isCorrect: false },
        { answerText: "Using a small dataset", isCorrect: false },
      ],
    },
    {
      questionText: "Which loss function is commonly used for binary classification?",
      answerOptions: [
        { answerText: "Mean Squared Error", isCorrect: false },
        { answerText: "Cross-Entropy Loss", isCorrect: true },
        { answerText: "Hinge Loss", isCorrect: false },
        { answerText: "Huber Loss", isCorrect: false },
      ],
    },
  ],
};


const colors = {
  background: "#121212",
  cardBg: "#1e1e1e",
  primary: "#BB86FC",
  correct: "#4CAF50",
  wrong: "#CF6679",
  textLight: "#E0E0E0",
  textDark: "#121212",
  buttonBg: "#3700B3",
  buttonHover: "#6200EE",
};

function App() {
  const [quizStarted, setQuizStarted] = useState(false); // new state to track quiz start
  const [selectedSubject, setSelectedSubject] = useState(null);
  const [currentQuestion, setCurrentQuestion] = useState(0);
  const [score, setScore] = useState(0);
  const [showScore, setShowScore] = useState(false);
  const [selectedAnswerIndex, setSelectedAnswerIndex] = useState(null);
  const [, setAnswerFeedback] = useState(null);

  const questions = selectedSubject ? allQuestions[selectedSubject] : [];

  const handleAnswerClick = (answerOption, index) => {
    if (selectedAnswerIndex !== null) return; // Prevent multiple clicks

    setSelectedAnswerIndex(index);

    if (answerOption.isCorrect) {
      setScore(score + 1);
      setAnswerFeedback("correct");
    } else {
      setAnswerFeedback("wrong");
    }

    setTimeout(() => {
      setSelectedAnswerIndex(null);
      setAnswerFeedback(null);

      if (currentQuestion + 1 < questions.length) {
        setCurrentQuestion(currentQuestion + 1);
      } else {
        setShowScore(true);
      }
    }, 1200);
  };

  const handleSubjectSelect = (subject) => {
    setSelectedSubject(subject);
    setCurrentQuestion(0);
    setScore(0);
    setShowScore(false);
    setSelectedAnswerIndex(null);
    setAnswerFeedback(null);
  };

  const handleStartQuiz = () => {
    setQuizStarted(true);
  };

  return (
    <div
      style={{
        backgroundColor: colors.background,
        minHeight: "100vh",
        color: colors.textLight,
        fontFamily: "'Segoe UI', Tahoma, Geneva, Verdana, sans-serif",
        display: "flex",
        justifyContent: "center",
        alignItems: "center",
        padding: 20,
      }}
    >
      <div
        style={{
          backgroundColor: colors.cardBg,
          borderRadius: 15,
          boxShadow: "0 8px 24px rgba(187,134,252,0.4)",
          maxWidth: 600,
          width: "100%",
          padding: 30,
          textAlign: "center",
          userSelect: "none",
        }}
      >
       {!quizStarted ? (
  <div>
    <h1 style={{ color: colors.primary, marginBottom: 10 }}>Welcome to the Ultimate Quiz Challenge!</h1>
    <p style={{ fontSize: 18, marginBottom: 30, color: colors.textLight, maxWidth: 480, margin: "auto" }}>
      Test your knowledge across different subjects. Click the Start button below to begin.
      Good luck and have fun!
    </p>
    <button
      onClick={handleStartQuiz}
      style={{
        backgroundColor: colors.buttonBg,
        color: colors.textLight,
        border: "none",
        padding: "16px 40px",
        fontSize: 22,
        borderRadius: 12,
        cursor: "pointer",
        boxShadow: "0 6px 20px rgba(103,58,183,0.7)",
        fontWeight: "700",
        transition: "background-color 0.3s ease",
      }}
      onMouseEnter={(e) => (e.target.style.backgroundColor = colors.buttonHover)}
      onMouseLeave={(e) => (e.target.style.backgroundColor = colors.buttonBg)}
    >
      Start Quiz
    </button>
  </div>
) : /* rest of your code */
 
 !selectedSubject ? (
          <>
            <h2 style={{ marginBottom: 25, color: colors.primary }}>Select a Subject</h2>
            <div
              style={{
                display: "flex",
                justifyContent: "center",
                gap: 20,
                flexWrap: "wrap",
              }}
            >
              {Object.keys(allQuestions).map((subject) => (
                <button
                  key={subject}
                  onClick={() => handleSubjectSelect(subject)}
                  style={{
                    backgroundColor: colors.buttonBg,
                    color: colors.textLight,
                    border: "none",
                    padding: "14px 28px",
                    fontSize: 18,
                    borderRadius: 10,
                    cursor: "pointer",
                    boxShadow: "0 4px 10px rgba(103,58,183,0.6)",
                    transition: "background-color 0.3s ease",
                    minWidth: 130,
                    textTransform: "capitalize",
                    fontWeight: "600",
                  }}
                  onMouseEnter={(e) => (e.target.style.backgroundColor = colors.buttonHover)}
                  onMouseLeave={(e) => (e.target.style.backgroundColor = colors.buttonBg)}
                >
                  {subject}
                </button>
              ))}
            </div>
          </>
        ) : showScore ? (
          <>
            <h3 style={{ color: colors.primary }}>
              You scored {score} out of {questions.length} in{" "}
              {selectedSubject.charAt(0).toUpperCase() + selectedSubject.slice(1)}
            </h3>
            <button
              onClick={() => {
                setSelectedSubject(null);
                setQuizStarted(false); // Reset quiz to start again
              }}
              style={{
                marginTop: 30,
                padding: "12px 28px",
                fontSize: 18,
                borderRadius: 10,
                border: "none",
                cursor: "pointer",
                backgroundColor: colors.buttonBg,
                color: colors.textLight,
                fontWeight: "600",
                boxShadow: "0 4px 12px rgba(103,58,183,0.7)",
                transition: "background-color 0.3s ease",
              }}
              onMouseEnter={(e) => (e.target.style.backgroundColor = colors.buttonHover)}
              onMouseLeave={(e) => (e.target.style.backgroundColor = colors.buttonBg)}
            >
              Choose Another Subject
            </button>
          </>
        ) : (
          <>
            <div
              style={{
                fontSize: 20,
                fontWeight: "700",
                marginBottom: 15,
                color: colors.primary,
              }}
            >
              Question {currentQuestion + 1} / {questions.length}
            </div>
            <div
              style={{
                fontSize: 22,
                fontWeight: "600",
                marginBottom: 30,
                lineHeight: 1.3,
                color: colors.textLight,
                minHeight: 80,
              }}
            >
              {questions[currentQuestion].questionText}
            </div>
            <div
              style={{
                display: "flex",
                flexDirection: "column",
                gap: 15,
              }}
            >
              {questions[currentQuestion].answerOptions.map((answerOption, index) => {
                const isSelected = selectedAnswerIndex === index;
                const isCorrectAnswer = answerOption.isCorrect;

                let bgColor = colors.cardBg;
                let color = colors.textLight;
                let boxShadow = "none";

                if (selectedAnswerIndex !== null) {
                  if (isSelected && isCorrectAnswer) {
                    bgColor = colors.correct;
                    color = colors.textDark;
                    boxShadow = `0 0 12px ${colors.correct}`;
                  } else if (isSelected && !isCorrectAnswer) {
                    bgColor = colors.wrong;
                    color = colors.textDark;
                    boxShadow = `0 0 12px ${colors.wrong}`;
                  } else if (isCorrectAnswer) {
                    bgColor = "#388E3C44"; // subtle green for correct answer
                    color = colors.textLight;
                  }
                }

                return (
                  <button
                    key={index}
                    onClick={() => handleAnswerClick(answerOption, index)}
                    disabled={selectedAnswerIndex !== null}
                    style={{
                      padding: "14px 20px",
                      fontSize: 18,
                      borderRadius: 12,
                      border: "2px solid transparent",
                      cursor: selectedAnswerIndex === null ? "pointer" : "default",
                      backgroundColor: bgColor,
                      color: color,
                      fontWeight: "600",
                      boxShadow: boxShadow,
                      transition: "all 0.3s ease",
                      textAlign: "left",
                      userSelect: "none",
                      minWidth: "100%",
                    }}
                    onMouseEnter={(e) => {
                      if (selectedAnswerIndex === null) {
                        e.target.style.backgroundColor = colors.primary;
                        e.target.style.color = colors.textDark;
                      }
                    }}
                    onMouseLeave={(e) => {
                      if (selectedAnswerIndex === null) {
                        e.target.style.backgroundColor = colors.cardBg;
                        e.target.style.color = colors.textLight;
                      }
                    }}
                  >
                    {answerOption.answerText}
                  </button>
                );
              })}
            </div>
          </>
        )}
      </div>
    </div>
  );
}

export default App;
