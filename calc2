<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Тест: Що заважає тобі заробляти?</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; }
        .question { margin-bottom: 10px; }
        .container { max-width: 600px; margin: auto; }
        button { padding: 10px; margin-top: 20px; cursor: pointer; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Тест: "Що заважає тобі заробляти?"</h1>
        <form id="roiTest">
            <div class="question">
                <label>1. Чи розподіляєте ви задачі між підлеглими, враховуючи їхню компетентність?</label><br>
                <input type="number" min="1" max="5" name="q1" required>
            </div>
            
            <div class="question">
                <label>2. Чи вкладаєтеся в навчання та розвиток ваших співробітників?</label><br>
                <input type="number" min="1" max="5" name="q2" required>
            </div>
            
            <div class="question">
                <label>3. Чи можете довірити підлеглим критично важливі завдання без необхідності постійного контролю?</label><br>
                <input type="number" min="1" max="5" name="q3" required>
            </div>
            
            <div class="question">
                <label>4. Який середній дохід приносить кожен співробітник після проходження навчання? (в доларах)</label><br>
                <input type="number" name="income" required>
            </div>
            
            <div class="question">
                <label>5. Які витрати на навчання одного співробітника? (в доларах)</label><br>
                <input type="number" name="cost" required>
            </div>
            
            <button type="button" onclick="calculateROI()">Розрахувати ROI</button>
        </form>
        <h2 id="result"></h2>
    </div>

    <script>
        function calculateROI() {
            let form = document.getElementById("roiTest");
            let totalScore = 0;
            let elements = form.elements;
            
            for (let i = 0; i < elements.length; i++) {
                if (elements[i].type === "number" && elements[i].name.startsWith("q")) {
                    totalScore += parseInt(elements[i].value) || 0;
                }
            }

            let income = parseFloat(elements["income"].value) || 0;
            let cost = parseFloat(elements["cost"].value) || 0;

            let roi = ((income - cost) / cost) * 100;
            let message = `Ваш загальний бал: ${totalScore}. ROI навчання: ${roi.toFixed(2)}%`;

            document.getElementById("result").innerText = message;
        }
    </script>
</body>
</html>
