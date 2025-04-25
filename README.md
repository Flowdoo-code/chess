
 # Chess Board

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chess Board</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .chess-board {
            display: grid;
            grid-template-columns: repeat(8, 1fr);
            width: 400px;
            height: 400px;
        }
        .chess-board div {
            width: 50px;
            height: 50px;
        }
        .black {
            background-color: #769656;
        }
        .white {
            background-color: #eeeed2;
        }
        .piece {
            font-size: 2em;
            text-align: center;
            line-height: 50px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="chess-board">
        <div class="white piece" onclick="movePiece(this)">♖</div>
        <div class="black piece" onclick="movePiece(this)">♘</div>
        <div class="white piece" onclick="movePiece(this)">♗</div>
        <div class="black piece" onclick="movePiece(this)">♕</div>
        <div class="white piece" onclick="movePiece(this)">♔</div>
        <div class="black piece" onclick="movePiece(this)">♗</div>
        <div class="white piece" onclick="movePiece(this)">♘</div>
        <div class="black piece" onclick="movePiece(this)">♖</div>
        <div class="black piece" onclick="movePiece(this)">♟</div>
        <div class="white piece" onclick="movePiece(this)">♟</div>
        <div class="black piece" onclick="movePiece(this)">♟</div>
        <div class="white piece" onclick="movePiece(this)">♟</div>
        <div class="black piece" onclick="movePiece(this)">♟</div>
        <div class="white piece" onclick="movePiece(this)">♟</div>
        <div class="black piece" onclick="movePiece(this)">♟</div>
        <div class="white piece" onclick="movePiece(this)">♟</div>
    </div>

    <script>
        function movePiece(piece) {
            // Logic to move the piece
            alert("Move the piece!");
        }
    </script>
</body>
</html>
