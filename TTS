
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Teka-Teki Silang Pahlawan Indonesia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Grid Crossword Styling */
        .crossword-grid {
            display: grid;
            grid-template-columns: repeat(10, 40px);
            grid-template-rows: repeat(10, 40px);
            gap: 2px;
            margin: 20px auto;
            max-width: 400px;
        }

        .crossword-cell {
            border: 1px solid #334155;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f9ff;
            transition: background-color 0.3s ease;
        }

        .crossword-cell.black {
            background-color: #334155;
        }

        .crossword-cell.number::before {
            content: attr(data-number);
            position: absolute;
            top: 2px;
            left: 2px;
            font-size: 10px;
            color: #1e293b;
            font-weight: bold;
        }

        .crossword-cell input {
            width: 100%;
            height: 100%;
            text-align: center;
            text-transform: uppercase;
            border: none;
            background: transparent;
            font-size: 16px;
        }

        .clue-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .clue-section {
            flex: 1;
            min-width: 300px;
        }
    </style>
</head>
<body class="bg-blue-50 p-8">
    <div class="container mx-auto">
        <h1 class="text-3xl font-bold text-center mb-6 text-blue-900">Teka-Teki Silang Pahlawan Indonesia</h1>
        
        <div class="crossword-grid">
            <!-- Grid akan dihasilkan oleh JavaScript -->
        </div>

        <div class="clue-list">
            <div class="clue-section">
                <h2 class="text-xl font-semibold mb-4">Mendatar</h2>
                <ol id="horizontal-clues" class="list-decimal pl-5">
                    <!-- Soal mendatar akan diisi -->
                </ol>
            </div>
            
            <div class="clue-section">
                <h2 class="text-xl font-semibold mb-4">Menurun</h2>
                <ol id="vertical-clues" class="list-decimal pl-5">
                    <!-- Soal menurun akan diisi -->
                </ol>
            </div>
        </div>
    </div>

    <script>
        const crosswordData = {
            grid: [
                [1, 0, 0, 0, 0, 0, 0, 0, 0, 2],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
                [3, 0, 0, 0, 0, 0, 0, 0, 0, 4]
            ],
            horizontalClues: [
                { number: 1, clue: "Panglima Perang dari Sulawesi Selatan yang memberontak melawan Belanda", answer: "SUPRIYADI" },
                { number: 2, clue: "Gubernur pertama Jawa Barat yang ikut berjuang kemerdekaan", answer: "SUTARJO" },
                { number: 3, clue: "Pahlawan dari Aceh yang memimpin perlawanan terhadap Belanda", answer: "TEUKU" },
                { number: 4, clue: "Nama pemimpin pemberontakan di Sulawesi Selatan", answer: "ANDI" }
            ],
            verticalClues: [
                { number: 1, clue: "Panglima Perang legendaris dari Jawa", answer: "DIPONEGORO" },
                { number: 2, clue: "Nama pejuang perempuan dari Sumatra", answer: "RASUNA" },
                { number: 3, clue: "Pejuang kemerdekaan dari Kalimantan", answer: "LAMBUNG" },
                { number: 4, clue: "Nama pahlawan yang diabadikan sebagai nama bandara di Jakarta", answer: "HALIM" }
            ]
        };

        function createCrosswordGrid() {
            const gridContainer = document.querySelector('.crossword-grid');
            const horizontalCluesList = document.getElementById('horizontal-clues');
            const verticalCluesList = document.getElementById('vertical-clues');

            crosswordData.grid.forEach((row, rowIndex) => {
                row.forEach((cell, colIndex) => {
                    const cellElement = document.createElement('div');
                    cellElement.classList.add('crossword-cell');

                    if (cell === 0) {
                        const input = document.createElement('input');
                        input.setAttribute('maxlength', '1');
                        input.setAttribute('data-row', rowIndex);
                        input.setAttribute('data-col', colIndex);
                        cellElement.appendChild(input);
                    } else {
                        cellElement.classList.add('number', 'black');
                        cellElement.setAttribute('data-number', cell);
                    }

                    gridContainer.appendChild(cellElement);
                });
            });

            // Tambahkan petunjuk mendatar
            crosswordData.horizontalClues.forEach(clue => {
                const li = document.createElement('li');
                li.innerHTML = `<strong>${clue.number}.</strong> ${clue.clue}`;
                horizontalCluesList.appendChild(li);
            });

            // Tambahkan petunjuk menurun
            crosswordData.verticalClues.forEach(clue => {
                const li = document.createElement('li');
                li.innerHTML = `<strong>${clue.number}.</strong> ${clue.clue}`;
                verticalCluesList.appendChild(li);
            });
        }

        // Inisialisasi Grid
        createCrosswordGrid();
    </script>
</body>
</html>
