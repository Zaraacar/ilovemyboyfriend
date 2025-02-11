# ilovemyboyfriend
i love you mo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Day for Mo</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-image: url('https://source.unsplash.com/1600x900/?cute-cat'); /* Süße Katzen */
            background-size: cover;
            color: white;
            padding-top: 100px;
        }
        h1 {
            font-size: 50px;
            text-shadow: 2px 2px 4px black;
        }
        .question {
            font-size: 30px;
            margin-top: 20px;
            text-shadow: 2px 2px 4px black;
        }
        #buttons {
            margin-top: 20px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
        }
        .yes {
            background-color: pink;
            color: white;
        }
        .no {
            background-color: lightgray;
            color: black;
        }
        #response {
            font-size: 30px;
            margin-top: 30px;
        }
        #cats {
            display: none;
            margin-top: 30px;
        }
        .cat {
            font-size: 50px;
            animation: dance 1s infinite;
        }
        @keyframes dance {
            0% { transform: rotate(0deg); }
            50% { transform: rotate(10deg); }
            100% { transform: rotate(-10deg); }
        }
    </style>
</head>
<body>

    <h1>Will you be my Valentine, Mo? 💖</h1>

    <!-- First Question: Will You Be My Valentine -->
    <div class="question" id="question1">Yes, please touch me now! Or No, you did not!</div>
    <div id="buttons">
        <button class="yes" onclick="nextQuestion('yes', 1)">Yes</button>
        <button class="no" onclick="nextQuestion('no', 1)">No</button>
    </div>

    <!-- Response after question 1 -->
    <div id="response" class="question"></div>

    <!-- Second Question: Can you touch me? -->
    <div class="question" id="question2" style="display:none;">Can you touch me?</div>
    <div id="buttons2" style="display:none;">
        <button class="yes" onclick="nextQuestion('yes', 2)">Yes</button>
    </div>

    <!-- Yay message -->
    <div id="yayMessage" style="display:none; font-size: 30px;">Yay!</div>

    <!-- Dancing Cats -->
    <div id="cats" style="display:none;">
        <h2>Here are some dancing cats! 🐱</h2>
        <div class="cat">🐾</div>
        <div class="cat">🐾</div>
        <div class="cat">🐾</div>
        <div class="cat">🐾</div>
    </div>

    <!-- Fourth Question: Do you love me? -->
    <div class="question" id="question3" style="display:none;">Do you love me?</div>
    <div id="buttons3" style="display:none;">
        <button class="yes" onclick="nextQuestion('yes', 3)">Yes</button>
        <button class="no" onclick="nextQuestion('no', 3)">No</button>
    </div>

    <!-- Response after question 3 -->
    <div id="response3" class="question" style="display:none;"></div>

    <!-- Zara + Mo -->
    <div id="zaramo" style="display:none;">
        <h2>Zara + Mo 💖</h2>
        <h3>Zara + Mo x 100! ❤️</h3>
    </div>

    <script>
        // Handles the flow of questions and responses
        function nextQuestion(answer, questionNumber) {
            if (questionNumber === 1) {
                // Handle first question response
                if (answer === 'yes') {
                    document.getElementById("response").innerHTML = "Yes, please touch me now!";
                } else {
                    document.getElementById("response").innerHTML = "You did not!";
                }
                document.getElementById("question1").style.display = 'none';
                document.getElementById("buttons").style.display = 'none';
                document.getElementById("response").style.display = 'block';
                setTimeout(() => {
                    document.getElementById("question2").style.display = 'block';
                    document.getElementById("buttons2").style.display = 'block';
                }, 2000);
            } else if (questionNumber === 2) {
                // Handle second question response
                document.getElementById("yayMessage").style.display = 'block';
                document.getElementById("question2").style.display = 'none';
                document.getElementById("buttons2").style.display = 'none';
                setTimeout(() => {
                    document.getElementById("cats").style.display = 'block';
                    setTimeout(() => {
                        document.getElementById("question3").style.display = 'block';
                        document.getElementById("buttons3").style.display = 'block';
                    }, 3000);
                }, 2000);
            } else if (questionNumber === 3) {
                // Handle third question response
                if (answer === 'yes') {
                    document.getElementById("response3").innerHTML = "I love you too!";
                } else {
                    document.getElementById("response3").innerHTML = "I love you, I still love you!";
                }
                document.getElementById("question3").style.display = 'none';
                document.getElementById("buttons3").style.display = 'none';
                document.getElementById("response3").style.display = 'block';
                setTimeout(() => {
                    document.getElementById("zaramo").style.display = 'block';
                }, 2000);
            }
        }
    </script>

</body>
</html>
