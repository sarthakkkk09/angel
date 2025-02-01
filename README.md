<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            background-color: #f9e8e8;
            font-family: 'Arial', sans-serif;
            text-align: center;
            color: #ff6f61;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        h1 {
            font-size: 2.5rem;
            margin: 20px 0;
        }

        .message {
            font-size: 1.5rem;
            margin: 20px 0;
            color: #ff6f61;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.1);
            display: inline-block;
        }

        .buttons {
            margin-top: 30px;
        }

        button {
            background-color: #ff6f61;
            border: none;
            color: white;
            font-size: 1.2rem;
            padding: 15px 25px;
            margin: 10px;
            cursor: pointer;
            border-radius: 50px;
            transition: transform 0.3s ease;
        }

        button:hover {
            background-color: #ff3e3b;
        }

        .no {
            transition: transform 0.3s ease;
        }

        /* When No is clicked, it flips */
        .flip {
            transform: rotate(180deg);
        }

        .heart {
            font-size: 3rem;
            color: #ff6f61;
        }

    </style>
</head>
<body>

    <h1>Will You Be My Valentine, Angel?</h1>
    <div class="message">
        <span class="heart">❤️</span>
        I have a question for you...
        <span class="heart">❤️</span>
    </div>

    <div class="buttons">
        <button id="yesButton">Yes</button>
        <button id="noButton" class="no">No</button>
    </div>

    <script>
        // Get the buttons
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');

        // When Yes button is clicked
        yesButton.addEventListener('click', () => {
            alert("Yay! I'm so happy you said yes! 💖");
            // You can add more functionality here, like redirecting to a new page or showing a new message.
        });

        // When No button is clicked
        noButton.addEventListener('click', () => {
            noButton.classList.add('flip'); // Apply the flip class to rotate the button
            setTimeout(() => {
                alert("Oops! That's okay! Still love you, Angel!");
            }, 300);
        });
    </script>

</body>
</html>
