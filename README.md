<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Puzzle Game for Farhan</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        .hidden {
            display: none;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 20px;
            cursor: pointer;
            border-radius: 5px;
            border: none;
        }
        button:hover {
            background-color: #f0f0f0;
        }
    </style>
</head>
<body>
    <h1>Welcome to the Puzzle Game!</h1>
    <div id="puzzle1">
        <p>What's your name?</p>
        <button onclick="showPuzzle2()">Farhan</button>
        <button onclick="doNothing()">No</button>
    </div>

    <div id="puzzle2" class="hidden">
        <p>Today is 6 December!</p>
        <button onclick="showFinalMessage()">Yes</button>
        <button onclick="doNothing()">No</button>
    </div>

    <div id="finalMessage" class="hidden">
        <h2>Happy Birthday My Lovely Fiance</h2>
        <p>Wish you a very very Happy Birthday 🎂🎈</p>
        <p>Happy or Not?</p>
        <button onclick="showKiss()">Yes</button>
        <button onclick="doNothing()">Not</button>
    </div>

    <div id="kiss" class="hidden">
        <h2>💋</h2>
        <p>That's it! Enjoy!</p>
    </div>

    <script>
        function showPuzzle2() {
            document.getElementById('puzzle1').classList.add('hidden');
            document.getElementById('puzzle2').classList.remove('hidden');
        }

        function showFinalMessage() {
            document.getElementById('puzzle2').classList.add('hidden');
            document.getElementById('finalMessage').classList.remove('hidden');
        }

        function showKiss() {
            document.getElementById('finalMessage').classList.add('hidden');
            document.getElementById('kiss').classList.remove('hidden');
        }

        function doNothing() {
            // If user clicks "No" nothing happens
        }
    </script>
</body>
</html>
