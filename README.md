# Chess Board

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chess Game</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        #chessboard {
            display: grid;
            grid-template-columns: repeat(8, 1fr);
            width: 400px;
            height: 400px;
        }
        .square {
            width: 50px;
            height: 50px;
        }
        .white {
            background-color: white;
        }
        .black {
            background-color: gray;
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
    <div id="chessboard"></div>
    <script>
        const board = document.getElementById('chessboard');
        const pieces = {
            'r': '♖', 'n': '♘', 'b': '♗', 'q': '♕', 'k': '♔', 'p': '♙',
            'R': '♜', 'N': '♞', 'B': '♟', 'Q': '♛', 'K': '♚', 'P': '♟'
        };
        const initialBoard = [
            'rnbqkbnr',
            'pppppppp',
            '........',
            '........',
            '........',
            '........',
            'PPPPPPPP',
            'RNBQKBNR'
        ];

        function createBoard() {
            initialBoard.forEach((row, rowIndex) => {
                row.split('').forEach((piece, colIndex) => {
                    const square = document.createElement('div');
                    square.className = 'square ' + ((rowIndex + colIndex) % 2 === 0 ? 'white' : 'black');
                    if (piece !== '.') {
                        const pieceElement = document.createElement('div');
                        pieceElement.className = 'piece';
                        pieceElement.innerHTML = pieces[piece];
                        square.appendChild(pieceElement);
                    }
                    board.appendChild(square);
                });
            });
        }

        createBoard();
    </script>
</body>
</html>
