# English-Steve
English
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Английский с Стивом | Полная версия</title>
    <style>
        /* Все стили остаются без изменений */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: linear-gradient(135deg, #58cc02, #4cb400);
            color: white;
            padding: 15px 20px;
            border-radius: 15px 15px 0 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .logo {
            display: flex;
            align-items: center;
            font-weight: bold;
            font-size: 24px;
        }

        .user-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .level-indicator {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 14px;
        }

        .header-buttons {
            display: flex;
            gap: 10px;
        }

        .header-btn {
            background-color: rgba(255, 255, 255, 0.2);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 14px;
        }

        .header-btn:hover {
            background-color: rgba(255, 255, 255, 0.3);
        }

        .progress-container {
            background-color: white;
            padding: 20px;
            border-radius: 0 0 15px 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }

        .progress-bar {
            height: 10px;
            background-color: #e0e0e0;
            border-radius: 5px;
            overflow: hidden;
            margin-top: 10px;
        }

        .progress {
            height: 100%;
            background: linear-gradient(135deg, #58cc02, #4cb400);
            width: 10%;
            transition: width 0.5s ease;
        }

        .main-content {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }

        .character-section {
            flex: 1;
            background-color: white;
            border-radius: 15px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .character {
            width: 150px;
            height: 150px;
            background-color: #f9f9f9;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 15px;
            position: relative;
            overflow: hidden;
        }

        .character img {
            width: 120px;
            height: 120px;
            transition: transform 0.3s ease;
        }

        .character.happy img {
            transform: scale(1.1);
        }

        .character.sad img {
            transform: scale(0.9);
        }

        .character-name {
            font-weight: bold;
            font-size: 18px;
            margin-bottom: 10px;
        }

        .timer-section {
            flex: 1;
            background-color: white;
            border-radius: 15px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .timer {
            font-size: 36px;
            font-weight: bold;
            color: #58cc02;
            margin: 10px 0;
        }

        .timer.warning {
            color: #ff9500;
        }

        .timer.danger {
            color: #ff3b30;
        }

        .task-section {
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }

        .task-title {
            font-size: 20px;
            margin-bottom: 15px;
            color: #4cb400;
        }

        .task-content {
            margin-bottom: 20px;
            font-size: 18px;
            line-height: 1.5;
        }

        .task-explanation {
            background-color: #f0f2f5;
            padding: 10px 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            font-size: 14px;
            color: #666;
        }

        .options {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 20px;
        }

        .option {
            background-color: #f0f2f5;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            padding: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            font-size: 16px;
        }

        .option:hover {
            background-color: #e8f5e8;
            border-color: #c0e0c0;
        }

        .option.selected {
            background-color: #e8f5e8;
            border-color: #58cc02;
        }

        .input-answer {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 16px;
            margin-bottom: 15px;
        }

        .input-answer:focus {
            border-color: #58cc02;
            outline: none;
        }

        .buttons {
            display: flex;
            justify-content: space-between;
            gap: 10px;
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }

        #check-btn {
            background: linear-gradient(135deg, #58cc02, #4cb400);
            color: white;
        }

        #check-btn:hover {
            background: linear-gradient(135deg, #4cb400, #3a9c00);
        }

        #hint-btn {
            background: linear-gradient(135deg, #ff9500, #ff7700);
            color: white;
        }

        #hint-btn:hover {
            background: linear-gradient(135deg, #ff7700, #ff5500);
        }

        #next-btn {
            background: linear-gradient(135deg, #1cb0f6, #0095e5);
            color: white;
        }

        #next-btn:hover {
            background: linear-gradient(135deg, #0095e5, #0077cc);
        }

        #pause-btn {
            background: linear-gradient(135deg, #ff9500, #ff7700);
            color: white;
        }

        #pause-btn:hover {
            background: linear-gradient(135deg, #ff7700, #ff5500);
        }

        #check-btn:disabled, #next-btn:disabled, #pause-btn:disabled, #hint-btn:disabled {
            background: #cccccc;
            cursor: not-allowed;
        }

        .feedback {
            margin-top: 15px;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            font-weight: bold;
            display: none;
        }

        .feedback.correct {
            background-color: #e8f5e8;
            color: #4cb400;
            display: block;
        }

        .feedback.incorrect {
            background-color: #ffe8e6;
            color: #ff3b30;
            display: block;
        }

        .feedback.hint {
            background-color: #fff4e6;
            color: #ff9500;
            display: block;
            text-align: left;
        }

        .hint-explanation {
            margin-top: 10px;
            padding: 10px;
            background-color: #fff9f0;
            border-radius: 8px;
            border-left: 4px solid #ff9500;
        }

        .hint-step {
            margin-bottom: 8px;
            padding-left: 10px;
        }

        .certificate-section {
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            text-align: center;
            display: none;
        }

        .certificate {
            border: 15px solid #58cc02;
            padding: 40px;
            margin: 20px auto;
            max-width: 700px;
            background: linear-gradient(135deg, #f9f9f9, #e8f5e8);
            position: relative;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .certificate:before {
            content: "";
            position: absolute;
            top: 10px;
            left: 10px;
            right: 10px;
            bottom: 10px;
            border: 2px solid #4cb400;
            pointer-events: none;
        }

        .certificate h2 {
            color: #4cb400;
            margin-bottom: 25px;
            font-size: 32px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .certificate p {
            margin-bottom: 15px;
            font-size: 18px;
            line-height: 1.6;
        }

        .certificate .level {
            font-size: 28px;
            font-weight: bold;
            color: #58cc02;
            margin: 25px 0;
            padding: 10px;
            border-top: 2px solid #4cb400;
            border-bottom: 2px solid #4cb400;
        }

        .levels-info {
            background-color: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

        .levels-info h3 {
            color: #4cb400;
            margin-bottom: 15px;
        }

        .level-description {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .level-item {
            flex: 1;
            min-width: 150px;
            padding: 10px;
            text-align: center;
            margin: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 8px;
        }

        .level-item:hover {
            background-color: #f0f2f5;
        }

        .level-item.current {
            background-color: #e8f5e8;
            border-radius: 8px;
        }

        .level-item h4 {
            color: #4cb400;
            margin-bottom: 5px;
        }

        .stats {
            background-color: white;
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            display: flex;
            justify-content: space-around;
            text-align: center;
        }

        .stat-item {
            padding: 10px;
        }

        .stat-value {
            font-size: 24px;
            font-weight: bold;
            color: #58cc02;
        }

        .stat-label {
            font-size: 14px;
            color: #666;
        }

        .level-selection {
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
            text-align: center;
        }

        .level-selection h2 {
            color: #4cb400;
            margin-bottom: 20px;
        }

        .level-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .level-card {
            background-color: #f9f9f9;
            border-radius: 12px;
            padding: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid #e0e0e0;
        }

        .level-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
            border-color: #58cc02;
        }

        .level-card.selected {
            border-color: #58cc02;
            background-color: #e8f5e8;
        }

        .level-card h3 {
            color: #4cb400;
            margin-bottom: 10px;
        }

        .level-card p {
            color: #666;
            font-size: 14px;
        }

        .celebrate-message {
            font-size: 24px;
            color: #ff6b00;
            margin: 20px 0;
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .signature {
            margin-top: 30px;
            display: flex;
            justify-content: space-between;
        }

        .signature-line {
            border-top: 1px solid #333;
            width: 200px;
            padding-top: 5px;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .options {
                grid-template-columns: 1fr;
            }
            
            .level-description {
                flex-direction: column;
            }
            
            .header-buttons {
                flex-direction: column;
                gap: 5px;
            }
            
            .level-grid {
                grid-template-columns: 1fr;
            }
            
            .buttons {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <span>Английский с Стивом</span>
            </div>
            <div class="user-info">
                <div class="level-indicator" id="level-indicator">Выберите уровень</div>
                <div class="header-buttons">
                    <button class="header-btn" id="change-level-btn">Сменить уровень</button>
                    <button class="header-btn" id="pause-btn">Пауза</button>
                </div>
            </div>
        </header>

        <!-- Экран выбора уровня -->
        <div class="level-selection" id="level-selection">
            <h2>Выберите уровень английского</h2>
            <p>Выберите уровень, соответствующий вашим знаниям и целям</p>
            <div class="level-grid">
                <div class="level-card" data-level="A1">
                    <h3>A1 (Начальный)</h3>
                    <p>Базовые фразы и выражения</p>
                    <p>~50 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="A1+">
                    <h3>A1+ (Начальный+)</h3>
                    <p>Основы грамматики и лексики</p>
                    <p>~10 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="A2">
                    <h3>A2 (Элементарный)</h3>
                    <p>Простые повседневные ситуации</p>
                    <p>~10 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B1">
                    <h3>B1 (Средний)</h3>
                    <p>Общение на знакомые темы</p>
                    <p>~10 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B1+">
                    <h3>B1+ (Средний+)</h3>
                    <p>Более сложные грамматические конструкции</p>
                    <p>~10 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B2">
                    <h3>B2 (Выше среднего)</h3>
                    <p>Сложные тексты и абстрактные темы</p>
                    <p>~10 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="C1">
                    <h3>C1 (Продвинутый)</h3>
                    <p>Свободное владение языком</p>
                    <p>~10 уникальных заданий</p>
                </div>
            </div>
        </div>

        <!-- Основной контент (скрыт до выбора уровня) -->
        <div id="main-content" style="display: none;">
            <div class="progress-container">
                <div>Прогресс уровня <span id="current-level-name">A1</span>: <span id="progress-percent">10%</span></div>
                <div class="progress-bar">
                    <div class="progress" id="progress"></div>
                </div>
            </div>

            <div class="main-content">
                <div class="character-section">
                    <div class="character happy" id="character">
                        <div style="width: 120px; height: 120px; background-color: #58cc02; border-radius: 50%; display: flex; justify-content: center; align-items: center; color: white; font-size: 60px;">S</div>
                    </div>
                    <div class="character-name">Стив</div>
                    <div id="character-message">Привет! Давай учить английский!</div>
                </div>

                <div class="timer-section">
                    <div>Время на задание:</div>
                    <div class="timer" id="timer">03:00</div>
                    <div>За каждое задание дается 3 минуты</div>
                </div>
            </div>

            <div class="task-section" id="task-section">
                <div class="task-title" id="task-title">Выберите правильный перевод</div>
                <div class="task-explanation" id="task-explanation">
                    <!-- Объяснение задания будет здесь -->
                </div>
                <div class="task-content" id="task-content">
                    Слово "house" переводится как:
                </div>
                <div class="options" id="options">
                    <div class="option" data-value="0">дом</div>
                    <div class="option" data-value="1">лошадь</div>
                    <div class="option" data-value="2">мышь</div>
                    <div class="option" data-value="3">час</div>
                </div>
                <div id="input-container" style="display: none;">
                    <input type="text" class="input-answer" id="input-answer" placeholder="Введите ваш ответ...">
                </div>
                <div class="buttons">
                    <button id="check-btn">Проверить</button>
                    <button id="hint-btn">Я не знаю</button>
                    <button id="next-btn" disabled>Далее</button>
                </div>
                <div class="feedback" id="feedback"></div>
            </div>

            <div class="stats">
                <div class="stat-item">
                    <div class="stat-value" id="completed-count">0</div>
                    <div class="stat-label">Выполнено заданий</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value" id="correct-count">0</div>
                    <div class="stat-label">Правильных ответов</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value" id="unique-tasks">0</div>
                    <div class="stat-label">Уникальных заданий</div>
                </div>
            </div>

            <div class="certificate-section" id="certificate-section">
                <div class="celebrate-message">🎉 Поздравляем с успешным завершением уровня! 🎉</div>
                <div class="certificate">
                    <h2>Сертификат об окончании</h2>
                    <p>Настоящим удостоверяется, что</p>
                    <p><strong>Ученик</strong></p>
                    <p>успешно завершил курс</p>
                    <p class="level">Английский язык - Уровень <span id="cert-level-name">A1</span></p>
                    <p>в соответствии с общеевропейскими компетенциями владения иностранным языком</p>
                    <p>Правильных ответов: <span id="certificate-score"></span> из <span id="certificate-total"></span></p>
                    <p>Дата: <span id="certificate-date"></span></p>
                    <div class="signature">
                        <div class="signature-line">Подпись преподавателя</div>
                        <div class="signature-line">Подпись директора</div>
                    </div>
                </div>
                <button id="restart-btn">Начать следующий уровень</button>
            </div>

            <div class="levels-info">
                <h3>Уровни английского языка</h3>
                <div class="level-description">
                    <div class="level-item current" data-level="A1">
                        <h4>A1</h4>
                        <p>Начальный</p>
                        <p>~50 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="A1+">
                        <h4>A1+</h4>
                        <p>Начальный+</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="A2">
                        <h4>A2</h4>
                        <p>Элементарный</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B1">
                        <h4>B1</h4>
                        <p>Средний</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B1+">
                        <h4>B1+</h4>
                        <p>Средний+</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B2">
                        <h4>B2</h4>
                        <p>Выше среднего</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="C1">
                        <h4>C1</h4>
                        <p>Продвинутый</p>
                        <p>~10 уникальных заданий</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Элементы DOM
            const levelSelection = document.getElementById('level-selection');
            const mainContent = document.getElementById('main-content');
            const levelIndicator = document.getElementById('level-indicator');
            const currentLevelName = document.getElementById('current-level-name');
            const changeLevelBtn = document.getElementById('change-level-btn');
            const levelCards = document.querySelectorAll('.level-card');
            const levelItems = document.querySelectorAll('.level-item');
            
            const character = document.getElementById('character');
            const characterMessage = document.getElementById('character-message');
            const timer = document.getElementById('timer');
            const progress = document.getElementById('progress');
            const progressPercent = document.getElementById('progress-percent');
            const taskTitle = document.getElementById('task-title');
            const taskExplanation = document.getElementById('task-explanation');
            const taskContent = document.getElementById('task-content');
            const optionsContainer = document.getElementById('options');
            const inputContainer = document.getElementById('input-container');
            const inputAnswer = document.getElementById('input-answer');
            const checkBtn = document.getElementById('check-btn');
            const hintBtn = document.getElementById('hint-btn');
            const nextBtn = document.getElementById('next-btn');
            const feedback = document.getElementById('feedback');
            const taskSection = document.getElementById('task-section');
            const certificateSection = document.getElementById('certificate-section');
            const certificateDate = document.getElementById('certificate-date');
            const certificateScore = document.getElementById('certificate-score');
            const certificateTotal = document.getElementById('certificate-total');
            const certificateLevelName = document.getElementById('certificate-level-name');
            const certLevelName = document.getElementById('cert-level-name');
            const restartBtn = document.getElementById('restart-btn');
            const completedCount = document.getElementById('completed-count');
            const correctCount = document.getElementById('correct-count');
            const uniqueTasks = document.getElementById('unique-tasks');
            const pauseBtn = document.getElementById('pause-btn');

            // Переменные состояния
            let currentQuestion = 0;
            let selectedOption = null;
            let timerInterval;
            let timeLeft = 180;
            let progressValue = 10;
            let questionsAnswered = 0;
            let correctAnswers = 0;
            let usedQuestionIds = new Set();
            let currentLevel = '';
            let questionBank = {};
            let currentTaskType = '';

            // Банк вопросов с РЕАЛЬНЫМИ вопросами для всех уровней
            questionBank = {
                'A1': [
                    // Базовые слова (20 заданий)
                    {
                        id: 1, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "house" переводится как:', options: ['дом', 'лошадь', 'мышь', 'час'], correct: 0,
                        hintSteps: ['Слово "house" является существительным в английском языке.', 'Оно переводится на русский язык как "дом".']
                    },
                    {
                        id: 2, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "book" переводится как:', options: ['книга', 'бокс', 'брать', 'готовить'], correct: 0,
                        hintSteps: ['Слово "book" означает "книга" на русском языке.']
                    },
                    {
                        id: 3, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "water" переводится как:', options: ['вода', 'погода', 'работа', 'слово'], correct: 0,
                        hintSteps: ['Слово "water" переводится как "вода".']
                    },
                    {
                        id: 4, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "big" переводится как:', options: ['большой', 'маленький', 'быстрый', 'медленный'], correct: 0,
                        hintSteps: ['Слово "big" означает "большой" на русском языке.']
                    },
                    {
                        id: 5, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "mother" переводится как:', options: ['мать', 'отец', 'сестра', 'брат'], correct: 0,
                        hintSteps: ['Слово "mother" переводится как "мать" на русском языке.']
                    },
                    {
                        id: 6, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "father" переводится как:', options: ['отец', 'брат', 'дядя', 'дедушка'], correct: 0,
                        hintSteps: ['Слово "father" переводится как "отец" на русском языке.']
                    },
                    {
                        id: 7, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "sister" переводится как:', options: ['сестра', 'брат', 'мать', 'дочь'], correct: 0,
                        hintSteps: ['Слово "sister" переводится как "сестра" на русском языке.']
                    },
                    {
                        id: 8, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "brother" переводится как:', options: ['брат', 'сестра', 'друг', 'сын'], correct: 0,
                        hintSteps: ['Слово "brother" переводится как "брат" на русском языке.']
                    },
                    {
                        id: 9, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "friend" переводится как:', options: ['друг', 'враг', 'сосед', 'коллега'], correct: 0,
                        hintSteps: ['Слово "friend" переводится как "друг" на русском языке.']
                    },
                    {
                        id: 10, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "school" переводится как:', options: ['школа', 'университет', 'колледж', 'детский сад'], correct: 0,
                        hintSteps: ['Слово "school" переводится как "школа" на русском языке.']
                    },
                    {
                        id: 11, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "teacher" переводится как:', options: ['учитель', 'ученик', 'директор', 'студент'], correct: 0,
                        hintSteps: ['Слово "teacher" переводится как "учитель" на русском языке.']
                    },
                    {
                        id: 12, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "student" переводится как:', options: ['студент', 'учитель', 'профессор', 'школьник'], correct: 0,
                        hintSteps: ['Слово "student" переводится как "студент" на русском языке.']
                    },
                    {
                        id: 13, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "city" переводится как:', options: ['город', 'деревня', 'страна', 'улица'], correct: 0,
                        hintSteps: ['Слово "city" переводится как "город" на русском языке.']
                    },
                    {
                        id: 14, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "country" переводится как:', options: ['страна', 'город', 'деревня', 'континент'], correct: 0,
                        hintSteps: ['Слово "country" переводится как "страна" на русском языке.']
                    },
                    {
                        id: 15, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "people" переводится как:', options: ['люди', 'человек', 'народ', 'личность'], correct: 0,
                        hintSteps: ['Слово "people" переводится как "люди" на русском языке.']
                    },
                    {
                        id: 16, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "time" переводится как:', options: ['время', 'раз', 'час', 'период'], correct: 0,
                        hintSteps: ['Слово "time" переводится как "время" на русском языке.']
                    },
                    {
                        id: 17, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "day" переводится как:', options: ['день', 'ночь', 'сутки', 'дата'], correct: 0,
                        hintSteps: ['Слово "day" переводится как "день" на русском языке.']
                    },
                    {
                        id: 18, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "night" переводится как:', options: ['ночь', 'день', 'вечер', 'утро'], correct: 0,
                        hintSteps: ['Слово "night" переводится как "ночь" на русском языке.']
                    },
                    {
                        id: 19, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "week" переводится как:', options: ['неделя', 'месяц', 'год', 'день'], correct: 0,
                        hintSteps: ['Слово "week" переводится как "неделя" на русском языке.']
                    },
                    {
                        id: 20, type: 'multiple-choice', question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "month" переводится как:', options: ['месяц', 'неделя', 'год', 'день'], correct: 0,
                        hintSteps: ['Слово "month" переводится как "месяц" на русском языке.']
                    },

                    // Глагол to be (10 заданий)
                    {
                        id: 21, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "I"',
                        content: 'I ___ a student.', options: ['am', 'is', 'are', 'be'], correct: 0,
                        hintSteps: ['Глагол "to be" имеет разные формы для разных лиц.', 'Для "I" (я) используется форма "am".']
                    },
                    {
                        id: 22, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "she"',
                        content: 'She ___ a teacher.', options: ['is', 'am', 'are', 'be'], correct: 0,
                        hintSteps: ['Для "she" (она) используется форма "is".']
                    },
                    {
                        id: 23, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "they"',
                        content: 'They ___ students.', options: ['are', 'is', 'am', 'be'], correct: 0,
                        hintSteps: ['Для "they" (они) используется форма "are".']
                    },
                    {
                        id: 24, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "we"',
                        content: 'We ___ friends.', options: ['are', 'is', 'am', 'be'], correct: 0,
                        hintSteps: ['Для "we" (мы) используется форма "are".']
                    },
                    {
                        id: 25, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "he"',
                        content: 'He ___ my brother.', options: ['is', 'am', 'are', 'be'], correct: 0,
                        hintSteps: ['Для "he" (он) используется форма "is".']
                    },
                    {
                        id: 26, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'My name ___ John.', correctAnswer: 'is',
                        hintSteps: ['Для третьего лица единственного числа используется форма "is".']
                    },
                    {
                        id: 27, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'I ___ from Russia.', correctAnswer: 'am',
                        hintSteps: ['Для первого лица единственного числа используется форма "am".']
                    },
                    {
                        id: 28, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'You ___ a good student.', correctAnswer: 'are',
                        hintSteps: ['Для второго лица используется форма "are".']
                    },
                    {
                        id: 29, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'It ___ a beautiful day.', correctAnswer: 'is',
                        hintSteps: ['Для третьего лица единственного числа используется форма "is".']
                    },
                    {
                        id: 30, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'We ___ happy to see you.', correctAnswer: 'are',
                        hintSteps: ['Для первого лица множественного числа используется форма "are".']
                    },

                    // Простые предложения (10 заданий)
                    {
                        id: 31, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'from / I / am / Russia', correctAnswer: 'I am from Russia',
                        hintSteps: ['Правильный порядок: "I am from Russia".']
                    },
                    {
                        id: 32, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'my / This / is / book', correctAnswer: 'This is my book',
                        hintSteps: ['Правильный порядок: "This is my book".']
                    },
                    {
                        id: 33, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'a / He / is / teacher', correctAnswer: 'He is a teacher',
                        hintSteps: ['Правильный порядок: "He is a teacher".']
                    },
                    {
                        id: 34, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'students / are / We', correctAnswer: 'We are students',
                        hintSteps: ['Правильный порядок: "We are students".']
                    },
                    {
                        id: 35, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'friend / My / is / this', correctAnswer: 'This is my friend',
                        hintSteps: ['Правильный порядок: "This is my friend".']
                    },
                    {
                        id: 36, type: 'multiple-choice', question: 'Выберите правильный перевод предложения',
                        explanation: 'Переведите предложение с английского на русский',
                        content: 'I am a student.', options: ['Я студент', 'Я учитель', 'Я доктор', 'Я инженер'], correct: 0,
                        hintSteps: ['Предложение "I am a student" переводится как "Я студент".']
                    },
                    {
                        id: 37, type: 'multiple-choice', question: 'Выберите правильный перевод предложения',
                        explanation: 'Переведите предложение с английского на русский',
                        content: 'She is from London.', options: ['Она из Лондона', 'Она в Лондоне', 'Она любит Лондон', 'Она знает Лондон'], correct: 0,
                        hintSteps: ['Предложение "She is from London" переводится как "Она из Лондона".']
                    },
                    {
                        id: 38, type: 'multiple-choice', question: 'Выберите правильный перевод предложения',
                        explanation: 'Переведите предложение с английского на русский',
                        content: 'We are happy.', options: ['Мы счастливы', 'Мы грустны', 'Мы устали', 'Мы заняты'], correct: 0,
                        hintSteps: ['Предложение "We are happy" переводится как "Мы счастливы".']
                    },
                    {
                        id: 39, type: 'multiple-choice', question: 'Выберите правильный перевод предложения',
                        explanation: 'Переведите предложение с английского на русский',
                        content: 'They are my friends.', options: ['Они мои друзья', 'Они мои братья', 'Они мои сестры', 'Они мои коллеги'], correct: 0,
                        hintSteps: ['Предложение "They are my friends" переводится как "Они мои друзья".']
                    },
                    {
                        id: 40, type: 'multiple-choice', question: 'Выберите правильный перевод предложения',
                        explanation: 'Переведите предложение с английского на русский',
                        content: 'It is a big house.', options: ['Это большой дом', 'Это маленький дом', 'Это новый дом', 'Это старый дом'], correct: 0,
                        hintSteps: ['Предложение "It is a big house" переводится как "Это большой дом".']
                    },

                    // Вопросы и отрицания (10 заданий)
                    {
                        id: 41, type: 'multiple-choice', question: 'Выберите правильную форму вопроса',
                        explanation: 'Выберите правильный порядок слов в вопросе',
                        content: '___ you a student?', options: ['Are', 'Is', 'Am', 'Be'], correct: 0,
                        hintSteps: ['Для вопроса со вторым лицом используется "Are".']
                    },
                    {
                        id: 42, type: 'multiple-choice', question: 'Выберите правильную форму вопроса',
                        explanation: 'Выберите правильный порядок слов в вопросе',
                        content: '___ she from England?', options: ['Is', 'Are', 'Am', 'Be'], correct: 0,
                        hintSteps: ['Для вопроса с третьим лицом единственного числа используется "Is".']
                    },
                    {
                        id: 43, type: 'multiple-choice', question: 'Выберите правильную форму вопроса',
                        explanation: 'Выберите правильный порядок слов в вопросе',
                        content: '___ they happy?', options: ['Are', 'Is', 'Am', 'Be'], correct: 0,
                        hintSteps: ['Для вопроса с третьим лицом множественного числа используется "Are".']
                    },
                    {
                        id: 44, type: 'multiple-choice', question: 'Выберите правильную форму отрицания',
                        explanation: 'Выберите правильную форму отрицания',
                        content: 'I ___ a teacher.', options: ['am not', 'is not', 'are not', 'not'], correct: 0,
                        hintSteps: ['Для первого лица единственного числа используется "am not".']
                    },
                    {
                        id: 45, type: 'multiple-choice', question: 'Выберите правильную форму отрицания',
                        explanation: 'Выберите правильную форму отрицания',
                        content: 'He ___ from France.', options: ['is not', 'am not', 'are not', 'not'], correct: 0,
                        hintSteps: ['Для третьего лица единственного числа используется "is not".']
                    },
                    {
                        id: 46, type: 'multiple-choice', question: 'Выберите правильную форму отрицания',
                        explanation: 'Выберите правильную форму отрицания',
                        content: 'We ___ tired.', options: ['are not', 'is not', 'am not', 'not'], correct: 0,
                        hintSteps: ['Для первого лица множественного числа используется "are not".']
                    },
                    {
                        id: 47, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму вопроса',
                        content: '___ this your book?', correctAnswer: 'Is',
                        hintSteps: ['Для вопроса с "this" используется "Is".']
                    },
                    {
                        id: 48, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму отрицания',
                        content: 'They ___ my classmates.', correctAnswer: 'are not',
                        hintSteps: ['Для отрицания с "they" используется "are not".']
                    },
                    {
                        id: 49, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму вопроса',
                        content: '___ I late?', correctAnswer: 'Am',
                        hintSteps: ['Для вопроса с "I" используется "Am".']
                    },
                    {
                        id: 50, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму отрицания',
                        content: 'She ___ here now.', correctAnswer: 'is not',
                        hintSteps: ['Для отрицания с "she" используется "is not".']
                    }
                ],

                'A1+': [
                    {
                        id: 51, type: 'multiple-choice', question: 'Выберите правильный артикль',
                        explanation: 'Выберите правильный неопределенный артикль',
                        content: 'I have ___ apple.', options: ['an', 'a', 'the', '-'], correct: 0,
                        hintSteps: ['Перед словами, начинающимися с гласного звука, используется "an".']
                    },
                    {
                        id: 52, type: 'multiple-choice', question: 'Выберите правильный артикль',
                        explanation: 'Выберите правильный неопределенный артикль',
                        content: 'She is ___ doctor.', options: ['a', 'an', 'the', '-'], correct: 0,
                        hintSteps: ['Перед словами, начинающимися с согласного звука, используется "a".']
                    },
                    {
                        id: 53, type: 'multiple-choice', question: 'Выберите правильный артикль',
                        explanation: 'Выберите правильный определенный артикль',
                        content: '___ sun is bright today.', options: ['The', 'A', 'An', '-'], correct: 0,
                        hintSteps: ['Для уникальных объектов используется "the".']
                    },
                    {
                        id: 54, type: 'multiple-choice', question: 'Выберите правильный предлог',
                        explanation: 'Выберите правильный предлог места',
                        content: 'The book is ___ the table.', options: ['on', 'in', 'at', 'under'], correct: 0,
                        hintSteps: ['Предлог "on" используется, когда что-то находится на поверхности.']
                    },
                    {
                        id: 55, type: 'multiple-choice', question: 'Выберите правильный предлог',
                        explanation: 'Выберите правильный предлог времени',
                        content: 'I go to school ___ Monday.', options: ['on', 'in', 'at', 'by'], correct: 0,
                        hintSteps: ['С днями недели используется предлог "on".']
                    },
                    {
                        id: 56, type: 'multiple-choice', question: 'Выберите правильную форму прилагательного',
                        explanation: 'Выберите правильную сравнительную степень',
                        content: 'My car is ___ than yours.', options: ['bigger', 'big', 'biggest', 'more big'], correct: 0,
                        hintSteps: ['Сравнительная степень прилагательного "big" - "bigger".']
                    },
                    {
                        id: 57, type: 'multiple-choice', question: 'Выберите правильную форму прилагательного',
                        explanation: 'Выберите правильную превосходную степень',
                        content: 'This is ___ building in the city.', options: ['the tallest', 'taller', 'tall', 'more tall'], correct: 0,
                        hintSteps: ['Превосходная степень прилагательного "tall" - "the tallest".']
                    },
                    {
                        id: 58, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное притяжательное местоимение',
                        content: 'This is ___ book. (мой)', correctAnswer: 'my',
                        hintSteps: ['Притяжательное местоимение "my" означает "мой".']
                    },
                    {
                        id: 59, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное указательное местоимение',
                        content: '___ is a pen. (это)', correctAnswer: 'This',
                        hintSteps: ['Указательное местоимение "this" означает "это" для близкого объекта.']
                    },
                    {
                        id: 60, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'my / This / is / book', correctAnswer: 'This is my book',
                        hintSteps: ['Правильный порядок: "This is my book".']
                    }
                ],

                'A2': [
                    {
                        id: 61, type: 'multiple-choice', question: 'Выберите правильное время глагола',
                        explanation: 'Выберите правильную форму глагола в Present Continuous',
                        content: 'They ___ football now.', options: ['are playing', 'play', 'plays', 'is playing'], correct: 0,
                        hintSteps: ['Present Continuous используется для действий, происходящих сейчас.']
                    },
                    {
                        id: 62, type: 'multiple-choice', question: 'Выберите правильное время глагола',
                        explanation: 'Выберите правильную форму глагола в Past Simple',
                        content: 'Yesterday I ___ to the cinema.', options: ['went', 'go', 'going', 'goes'], correct: 0,
                        hintSteps: ['Past Simple используется для действий в прошлом.']
                    },
                    {
                        id: 63, type: 'multiple-choice', question: 'Выберите правильное время глагола',
                        explanation: 'Выберите правильную форму глагола в Future Simple',
                        content: 'I think it ___ tomorrow.', options: ['will rain', 'rain', 'rains', 'raining'], correct: 0,
                        hintSteps: ['Future Simple используется для будущих действий.']
                    },
                    {
                        id: 64, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Present Perfect',
                        content: 'I ___ never ___ to London.', options: ['have, been', 'has, been', 'am, been', 'was, been'], correct: 0,
                        hintSteps: ['Present Perfect используется для опыта.']
                    },
                    {
                        id: 65, type: 'multiple-choice', question: 'Выберите правильный модальный глагол',
                        explanation: 'Выберите правильный модальный глагол для выражения возможности',
                        content: 'I ___ swim when I was five.', options: ['could', 'can', 'may', 'should'], correct: 0,
                        hintSteps: ['Модальный глагол "could" выражает возможность в прошлом.']
                    },
                    {
                        id: 66, type: 'multiple-choice', question: 'Выберите правильный модальный глагол',
                        explanation: 'Выберите правильный модальный глагол для выражения совета',
                        content: 'You ___ see a doctor.', options: ['should', 'can', 'must', 'will'], correct: 0,
                        hintSteps: ['Модальный глагол "should" выражает совет.']
                    },
                    {
                        id: 67, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное вопросительное слово',
                        content: '___ is your name?', correctAnswer: 'What',
                        hintSteps: ['Вопрос о имени обычно задается с помощью слова "What".']
                    },
                    {
                        id: 68, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное наречие частоты',
                        content: 'I ___ go to the gym. (часто)', correctAnswer: 'often',
                        hintSteps: ['Наречие "often" означает "часто".']
                    },
                    {
                        id: 69, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'often / I / to / go / cinema / the', correctAnswer: 'I often go to the cinema',
                        hintSteps: ['Правильный порядок: "I often go to the cinema".']
                    },
                    {
                        id: 70, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'did / What / you / do / yesterday?', correctAnswer: 'What did you do yesterday?',
                        hintSteps: ['Правильный порядок: "What did you do yesterday?".']
                    }
                ],

                'B1': [
                    {
                        id: 71, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Past Perfect',
                        content: 'She ___ already ___ when I arrived.', options: ['had, left', 'has, left', 'have, left', 'was, leaving'], correct: 0,
                        hintSteps: ['Past Perfect используется для действия, которое произошло до другого действия в прошлом.']
                    },
                    {
                        id: 72, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в условном предложении первого типа',
                        content: 'If it rains, we ___ at home.', options: ['will stay', 'stay', 'stayed', 'would stay'], correct: 0,
                        hintSteps: ['Условные предложения первого типа: If + Present Simple, will + инфинитив.']
                    },
                    {
                        id: 73, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Present Perfect Continuous',
                        content: 'They ___ for three hours.', options: ['have been working', 'have worked', 'are working', 'work'], correct: 0,
                        hintSteps: ['Present Perfect Continuous используется для действий, которые начались в прошлом и продолжаются до настоящего момента.']
                    },
                    {
                        id: 74, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в пассивном залоге',
                        content: 'The letter ___ yesterday.', options: ['was sent', 'sent', 'has sent', 'sends'], correct: 0,
                        hintSteps: ['Пассивный залог в Past Simple: was/were + причастие прошедшего времени.']
                    },
                    {
                        id: 75, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в условном предложении второго типа',
                        content: 'If I ___ you, I would study more.', options: ['were', 'am', 'was', 'would be'], correct: 0,
                        hintSteps: ['Условные предложения второго типа: If + Past Simple, would + инфинитив.']
                    },
                    {
                        id: 76, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное относительное местоимение',
                        content: 'This is the book ___ I bought yesterday.', correctAnswer: 'that',
                        hintSteps: ['Относительное местоимение "that" используется для определения.']
                    },
                    {
                        id: 77, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильный фразовый глагол',
                        content: 'I need to ___ ___ my homework. (закончить)', correctAnswer: 'finish up',
                        hintSteps: ['Фразовый глагол "finish up" означает "закончить".']
                    },
                    {
                        id: 78, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в условном предложении',
                        content: 'if / I / time / have / will / I / come', correctAnswer: 'If I have time, I will come',
                        hintSteps: ['Правильный порядок: "If I have time, I will come".']
                    },
                    {
                        id: 79, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в косвенной речи',
                        content: 'She / said / she / was / tired', correctAnswer: 'She said she was tired',
                        hintSteps: ['Правильный порядок: "She said she was tired".']
                    },
                    {
                        id: 80, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов с наречием',
                        content: 'never / He / has / been / to / Paris', correctAnswer: 'He has never been to Paris',
                        hintSteps: ['Правильный порядок: "He has never been to Paris".']
                    }
                ],

                'B1+': [
                    {
                        id: 81, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Passive Voice',
                        content: 'The book ___ by a famous author.', options: ['was written', 'written', 'wrote', 'has written'], correct: 0,
                        hintSteps: ['Passive Voice используется, когда подлежащее испытывает действие.']
                    },
                    {
                        id: 82, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Past Perfect Continuous',
                        content: 'They ___ for two hours when I arrived.', options: ['had been waiting', 'have been waiting', 'were waiting', 'waited'], correct: 0,
                        hintSteps: ['Past Perfect Continuous используется для действия, которое длилось до другого действия в прошлом.']
                    },
                    {
                        id: 83, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Future Perfect',
                        content: 'By next year, I ___ my degree.', options: ['will have completed', 'will complete', 'complete', 'have completed'], correct: 0,
                        hintSteps: ['Future Perfect используется для действия, которое завершится к определенному моменту в будущем.']
                    },
                    {
                        id: 84, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в условном предложении третьего типа',
                        content: 'If I ___ known, I would have helped.', options: ['had', 'have', 'would have', 'has'], correct: 0,
                        hintSteps: ['Условные предложения третьего типа: If + Past Perfect, would have + причастие прошедшего времени.']
                    },
                    {
                        id: 85, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Future Continuous',
                        content: 'This time tomorrow, I ___ to London.', options: ['will be flying', 'will fly', 'am flying', 'fly'], correct: 0,
                        hintSteps: ['Future Continuous используется для действия, которое будет происходить в определенный момент в будущем.']
                    },
                    {
                        id: 86, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильное сослагательное наклонение',
                        content: 'I suggest that he ___ the meeting.', correctAnswer: 'attend',
                        hintSteps: ['После глагола "suggest" используется сослагательное наклонение.']
                    },
                    {
                        id: 87, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильный инфинитив',
                        content: 'She seems ___ the answer.', correctAnswer: 'to know',
                        hintSteps: ['После глагола "seem" используется инфинитив с to.']
                    },
                    {
                        id: 88, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в сложном предложении',
                        content: 'Although / he / tired / was / he / working / continued', correctAnswer: 'Although he was tired, he continued working',
                        hintSteps: ['Правильный порядок: "Although he was tired, he continued working".']
                    },
                    {
                        id: 89, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов с инверсией',
                        content: 'Never / I / have / such / seen / a / beautiful / place', correctAnswer: 'Never have I seen such a beautiful place',
                        hintSteps: ['Правильный порядок: "Never have I seen such a beautiful place".']
                    },
                    {
                        id: 90, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в пассивном залоге',
                        content: 'The / cake / was / by / eaten / the / children', correctAnswer: 'The cake was eaten by the children',
                        hintSteps: ['Правильный порядок: "The cake was eaten by the children".']
                    }
                ],

                'B2': [
                    {
                        id: 91, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в условном предложении смешанного типа',
                        content: 'If I ___ about the meeting, I would have attended.', options: ['had known', 'have known', 'would know', 'knew'], correct: 0,
                        hintSteps: ['Смешанное условное предложение: условие в Past Perfect, результат в would + инфинитив.']
                    },
                    {
                        id: 92, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Future Perfect Continuous',
                        content: 'By 2025, I ___ here for 10 years.', options: ['will have been working', 'will work', 'have been working', 'will be working'], correct: 0,
                        hintSteps: ['Future Perfect Continuous используется для действия, которое будет длиться до определенного момента в будущем.']
                    },
                    {
                        id: 93, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Past Perfect Passive',
                        content: 'The project ___ by the time we arrived.', options: ['had been completed', 'has been completed', 'was completed', 'completed'], correct: 0,
                        hintSteps: ['Past Perfect Passive: had been + причастие прошедшего времени.']
                    },
                    {
                        id: 94, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Present Perfect Passive',
                        content: 'The decision ___ already ___.', options: ['has, been made', 'have, been made', 'was, made', 'is, made'], correct: 0,
                        hintSteps: ['Present Perfect Passive: have/has been + причастие прошедшего времени.']
                    },
                    {
                        id: 95, type: 'multiple-choice', question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в Future Passive',
                        content: 'The new building ___ next year.', options: ['will be built', 'will build', 'is built', 'builds'], correct: 0,
                        hintSteps: ['Future Passive: will be + причастие прошедшего времени.']
                    },
                    {
                        id: 96, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму герундия',
                        content: 'I look forward to ___ from you.', correctAnswer: 'hearing',
                        hintSteps: ['После выражения "look forward to" используется герундий.']
                    },
                    {
                        id: 97, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму инфинитива',
                        content: 'He is too young ___ drive.', correctAnswer: 'to',
                        hintSteps: ['После конструкции "too + прилагательное" используется инфинитив с to.']
                    },
                    {
                        id: 98, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в условном предложении смешанного типа',
                        content: 'If / she / studied / she / would / have / passed / harder', correctAnswer: 'If she had studied harder, she would have passed',
                        hintSteps: ['Правильный порядок: "If she had studied harder, she would have passed".']
                    },
                    {
                        id: 99, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов с инверсией',
                        content: 'Not only / he / late / was / but / he / also / forgot / his / books', correctAnswer: 'Not only was he late, but he also forgot his books',
                        hintSteps: ['Правильный порядок: "Not only was he late, but he also forgot his books".']
                    },
                    {
                        id: 100, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильный порядок слов в сложном предложении',
                        content: 'Despite / the / rain / we / decided / to / go / for / a / walk', correctAnswer: 'Despite the rain, we decided to go for a walk',
                        hintSteps: ['Правильный порядок: "Despite the rain, we decided to go for a walk".']
                    }
                ],

                'C1': [
                    {
                        id: 101, type: 'multiple-choice', question: 'Выберите правильную идиому',
                        explanation: 'Выберите правильное значение идиомы',
                        content: '"To bite the bullet" means:', options: ['to endure a painful experience', 'to eat something hard', 'to attack someone', 'to make a mistake'], correct: 0,
                        hintSteps: ['Идиома "to bite the bullet" означает стойко переносить неприятную или болезненную ситуацию.']
                    },
                    {
                        id: 102, type: 'multiple-choice', question: 'Выберите правильную идиому',
                        explanation: 'Выберите правильное значение идиомы',
                        content: '"To break the ice" means:', options: ['to make people feel more comfortable', 'to destroy something', 'to be cold', 'to fall through ice'], correct: 0,
                        hintSteps: ['Идиома "to break the ice" означает сделать так, чтобы люди чувствовали себя более комфортно в социальной ситуации.']
                    },
                    {
                        id: 103, type: 'multiple-choice', question: 'Выберите правильную идиому',
                        explanation: 'Выберите правильное значение идиомы',
                        content: '"To hit the nail on the head" means:', options: ['to describe exactly what is true', 'to make a mistake', 'to be angry', 'to work hard'], correct: 0,
                        hintSteps: ['Идиома "to hit the nail on the head" означает точно описать суть проблемы или ситуации.']
                    },
                    {
                        id: 104, type: 'multiple-choice', question: 'Выберите правильную идиому',
                        explanation: 'Выберите правильное значение идиомы',
                        content: '"To let the cat out of the bag" means:', options: ['to reveal a secret', 'to free an animal', 'to make a mistake', 'to be careless'], correct: 0,
                        hintSteps: ['Идиома "to let the cat out of the bag" означает раскрыть секрет, обычно случайно.']
                    },
                    {
                        id: 105, type: 'multiple-choice', question: 'Выберите правильную идиому',
                        explanation: 'Выберите правильное значение идиомы',
                        content: '"To be over the moon" means:', options: ['to be extremely happy', 'to be crazy', 'to be confused', 'to be tired'], correct: 0,
                        hintSteps: ['Идиома "to be over the moon" означает быть чрезвычайно счастливым.']
                    },
                    {
                        id: 106, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную идиому',
                        content: 'After working for 12 hours, I\'m completely ___.', correctAnswer: 'burned out',
                        hintSteps: ['Идиома "burned out" означает полное физическое и эмоциональное истощение.']
                    },
                    {
                        id: 107, type: 'fill-blank', question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную идиому',
                        content: 'We need to ___ and make a decision.', correctAnswer: 'bite the bullet',
                        hintSteps: ['Идиома "bite the bullet" означает принять трудное решение или стойко перенести неприятность.']
                    },
                    {
                        id: 108, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильную идиому в предложении',
                        content: 'the / ice / He / joke / told / a / to / break', correctAnswer: 'He told a joke to break the ice',
                        hintSteps: ['Правильный порядок: "He told a joke to break the ice".']
                    },
                    {
                        id: 109, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильную идиому в предложении',
                        content: 'nail / on / the / head / You / hit / the', correctAnswer: 'You hit the nail on the head',
                        hintSteps: ['Правильный порядок: "You hit the nail on the head".']
                    },
                    {
                        id: 110, type: 'sentence-builder', question: 'Составьте правильное предложение',
                        explanation: 'Используйте правильную идиому в предложении',
                        content: 'over / the / moon / She / was / with / her / results', correctAnswer: 'She was over the moon with her results',
                        hintSteps: ['Правильный порядок: "She was over the moon with her results".']
                    }
                ]
            };

            // Остальной код остается без изменений
            // Инициализация приложения
            function init() {
                // Если уровень уже выбран, загружаем его
                const savedLevel = localStorage.getItem('englishCurrentLevel');
                if (savedLevel) {
                    selectLevel(savedLevel);
                } else {
                    // Показываем экран выбора уровня
                    levelSelection.style.display = 'block';
                    mainContent.style.display = 'none';
                }
                
                setupEventListeners();
                setCertificateDate();
            }

            // Выбор уровня
            function selectLevel(level) {
                currentLevel = level;
                localStorage.setItem('englishCurrentLevel', level);
                
                // Обновляем интерфейс
                levelIndicator.textContent = `Уровень ${level}`;
                currentLevelName.textContent = level;
                
                // Показываем основной контент
                levelSelection.style.display = 'none';
                mainContent.style.display = 'block';
                
                // Обновляем выделение текущего уровня
                levelItems.forEach(item => {
                    if (item.getAttribute('data-level') === level) {
                        item.classList.add('current');
                    } else {
                        item.classList.remove('current');
                    }
                });
                
                // Сбрасываем прогресс для нового уровня
                resetProgress();
                
                // Загружаем вопросы для выбранного уровня
                if (!questionBank[level]) {
                    // Если для уровня нет вопросов, используем A1
                    questionBank[level] = questionBank['A1'];
                }
                
                // Запускаем таймер и загружаем первый вопрос
                startTimer();
                loadRandomQuestion();
                updateProgress();
                updateStats();
                
                // Скрываем сертификат и показываем задания
                certificateSection.style.display = 'none';
                taskSection.style.display = 'block';
            }

            // Установка даты в сертификате
            function setCertificateDate() {
                const today = new Date();
                const options = { year: 'numeric', month: 'long', day: 'numeric' };
                certificateDate.textContent = today.toLocaleDateString('ru-RU', options);
            }

            // Настройка обработчиков событий
            function setupEventListeners() {
                // Выбор уровня
                levelCards.forEach(card => {
                    card.addEventListener('click', function() {
                        const level = this.getAttribute('data-level');
                        selectLevel(level);
                    });
                });
                
                // Смена уровня
                changeLevelBtn.addEventListener('click', function() {
                    levelSelection.style.display = 'block';
                    mainContent.style.display = 'none';
                    certificateSection.style.display = 'none';
                    taskSection.style.display = 'none';
                });
                
                // Выбор уровня из списка внизу
                levelItems.forEach(item => {
                    item.addEventListener('click', function() {
                        const level = this.getAttribute('data-level');
                        selectLevel(level);
                    });
                });

                // Выбор варианта ответа
                optionsContainer.addEventListener('click', function(e) {
                    if (e.target.classList.contains('option')) {
                        // Снимаем выделение со всех вариантов
                        document.querySelectorAll('.option').forEach(opt => {
                            opt.classList.remove('selected');
                        });
                        
                        // Выделяем выбранный вариант
                        e.target.classList.add('selected');
                        selectedOption = parseInt(e.target.getAttribute('data-value'));
                        
                        // Активируем кнопку проверки
                        checkBtn.disabled = false;
                    }
                });

                // Ввод текста
                inputAnswer.addEventListener('input', function() {
                    if (inputAnswer.value.trim() !== '') {
                        checkBtn.disabled = false;
                    } else {
                        checkBtn.disabled = true;
                    }
                });

                // Проверка ответа
                checkBtn.addEventListener('click', checkAnswer);

                // Кнопка "Я не знаю"
                hintBtn.addEventListener('click', showHint);

                // Следующий вопрос
                nextBtn.addEventListener('click', nextQuestion);

                // Перезапуск
                restartBtn.addEventListener('click', function() {
                    const levelsOrder = ['A1', 'A1+', 'A2', 'B1', 'B1+', 'B2', 'C1'];
                    const currentIndex = levelsOrder.indexOf(currentLevel);
                    const nextLevel = levelsOrder[currentIndex + 1];
                    
                    if (nextLevel) {
                        selectLevel(nextLevel);
                        characterMessage.textContent = `Отлично! Теперь вы на уровне ${nextLevel}. Задания будут сложнее!`;
                    } else {
                        alert('Поздравляем! Вы завершили все уровни!');
                        // Возвращаем к выбору уровня
                        levelSelection.style.display = 'block';
                        mainContent.style.display = 'none';
                        certificateSection.style.display = 'none';
                    }
                });

                // Пауза
                pauseBtn.addEventListener('click', function() {
                    alert('Обучение на паузе. Для продолжения обновите страницу.');
                });
            }

            // Загрузка случайного вопроса
            function loadRandomQuestion() {
                // Если все вопросы использованы, показываем сертификат
                if (usedQuestionIds.size >= questionBank[currentLevel].length) {
                    showCertificate();
                    return;
                }
                
                // Выбираем случайный неиспользованный вопрос
                let availableQuestions = questionBank[currentLevel].filter(q => !usedQuestionIds.has(q.id));
                if (availableQuestions.length === 0) {
                    showCertificate();
                    return;
                }
                
                const randomIndex = Math.floor(Math.random() * availableQuestions.length);
                const q = availableQuestions[randomIndex];
                usedQuestionIds.add(q.id);
                currentTaskType = q.type;
                
                taskTitle.textContent = q.question;
                taskExplanation.textContent = q.explanation;
                taskContent.textContent = q.content;
                
                // Настройка интерфейса в зависимости от типа задания
                if (q.type === 'multiple-choice') {
                    optionsContainer.style.display = 'grid';
                    inputContainer.style.display = 'none';
                    
                    // Очищаем варианты ответов
                    optionsContainer.innerHTML = '';
                    
                    // Добавляем новые варианты ответов
                    q.options.forEach((option, index) => {
                        const optionElement = document.createElement('div');
                        optionElement.classList.add('option');
                        optionElement.setAttribute('data-value', index);
                        optionElement.textContent = option;
                        optionsContainer.appendChild(optionElement);
                    });
                } else if (q.type === 'fill-blank') {
                    optionsContainer.style.display = 'none';
                    inputContainer.style.display = 'block';
                    inputAnswer.value = '';
                    inputAnswer.placeholder = 'Введите слово...';
                    
                    // Добавляем подсказку
                    if (q.hint) {
                        taskExplanation.textContent = q.explanation + ` (Подсказка: ${q.hint})`;
                    }
                } else if (q.type === 'sentence-builder') {
                    optionsContainer.style.display = 'none';
                    inputContainer.style.display = 'block';
                    inputAnswer.value = '';
                    inputAnswer.placeholder = 'Введите предложение...';
                }
                
                // Сбрасываем состояние
                selectedOption = null;
                checkBtn.disabled = true;
                hintBtn.disabled = false;
                nextBtn.disabled = true;
                feedback.className = 'feedback';
                feedback.style.display = 'none';
                
                // Сбрасываем таймер
                resetTimer();
                
                // Обновляем статистику уникальных заданий
                updateStats();
            }

            // Проверка ответа
            function checkAnswer() {
                const q = questionBank[currentLevel].find(question => question.id === Array.from(usedQuestionIds).pop());
                let isCorrect = false;
                
                if (currentTaskType === 'multiple-choice') {
                    isCorrect = selectedOption === q.correct;
                } else if (currentTaskType === 'fill-blank' || currentTaskType === 'sentence-builder') {
                    const userAnswer = inputAnswer.value.trim().toLowerCase();
                    const correctAnswer = q.correctAnswer.toLowerCase();
                    isCorrect = userAnswer === correctAnswer;
                }
                
                if (isCorrect) {
                    feedback.textContent = 'Правильно! Молодец!';
                    feedback.className = 'feedback correct';
                    character.className = 'character happy';
                    characterMessage.textContent = getRandomHappyMessage();
                    correctAnswers += 1;
                    correctCount.textContent = correctAnswers.toFixed(1);
                } else {
                    feedback.textContent = `Неправильно. Правильный ответ: ${getCorrectAnswerText(q)}`;
                    feedback.className = 'feedback incorrect';
                    character.className = 'character sad';
                    characterMessage.textContent = getRandomSadMessage();
                }
                
                feedback.style.display = 'block';
                checkBtn.disabled = true;
                hintBtn.disabled = true;
                nextBtn.disabled = false;
                
                // Обновляем прогресс
                questionsAnswered++;
                completedCount.textContent = questionsAnswered;
                progressValue = Math.min(100, 10 + (questionsAnswered / questionBank[currentLevel].length) * 90);
                updateProgress();
                
                // Останавливаем таймер
                clearInterval(timerInterval);
            }

            // Показать подсказку
            function showHint() {
                const q = questionBank[currentLevel].find(question => question.id === Array.from(usedQuestionIds).pop());
                
                feedback.innerHTML = `
                    <div>Использована подсказка. Вы получаете 0.5 балла.</div>
                    <div class="hint-explanation">
                        <strong>Пошаговое объяснение:</strong>
                        ${q.hintSteps.map(step => `<div class="hint-step">${step}</div>`).join('')}
                    </div>
                `;
                feedback.className = 'feedback hint';
                feedback.style.display = 'block';
                
                character.className = 'character happy';
                characterMessage.textContent = 'Хорошо, что ты спросил! Теперь ты знаешь правильный ответ!';
                
                // Начисляем половину балла
                correctAnswers += 0.5;
                correctCount.textContent = correctAnswers.toFixed(1);
                
                // Обновляем прогресс
                questionsAnswered++;
                completedCount.textContent = questionsAnswered;
                progressValue = Math.min(100, 10 + (questionsAnswered / questionBank[currentLevel].length) * 90);
                updateProgress();
                
                // Отключаем кнопки и активируем "Далее"
                checkBtn.disabled = true;
                hintBtn.disabled = true;
                nextBtn.disabled = false;
                
                // Останавливаем таймер
                clearInterval(timerInterval);
            }

            // Получить текст правильного ответа
            function getCorrectAnswerText(question) {
                if (question.type === 'multiple-choice') {
                    return question.options[question.correct];
                } else if (question.type === 'fill-blank' || question.type === 'sentence-builder') {
                    return question.correctAnswer;
                }
                return '';
            }

            // Случайные сообщения для Стива
            function getRandomHappyMessage() {
                const messages = [
                    'Отлично! Так держать!',
                    'Превосходно! Ты молодец!',
                    'Ура! Правильный ответ!',
                    'Ты умничка! Продолжай в том же духе!',
                    'Браво! Ты справляешься великолепно!'
                ];
                return messages[Math.floor(Math.random() * messages.length)];
            }

            function getRandomSadMessage() {
                const messages = [
                    'Не расстраивайся! Попробуй еще!',
                    'Ничего страшного! В следующий раз получится!',
                    'Ошибка - это часть обучения! Продолжай!',
                    'Не сдавайся! Ты сможешь!',
                    'Попробуй еще раз! У тебя все получится!'
                ];
                return messages[Math.floor(Math.random() * messages.length)];
            }

            // Следующий вопрос
            function nextQuestion() {
                loadRandomQuestion();
            }

            // Показать сертификат
            function showCertificate() {
                taskSection.style.display = 'none';
                certificateSection.style.display = 'block';
                progressValue = 100;
                updateProgress();
                certificateScore.textContent = correctAnswers.toFixed(1);
                certificateTotal.textContent = questionsAnswered;
                certificateLevelName.textContent = currentLevel;
                certLevelName.textContent = currentLevel;
            }

            // Сброс прогресса
            function resetProgress() {
                usedQuestionIds.clear();
                progressValue = 10;
                questionsAnswered = 0;
                correctAnswers = 0;
                updateProgress();
                updateStats();
            }

            // Обновление прогресса
            function updateProgress() {
                progress.style.width = `${progressValue}%`;
                progressPercent.textContent = `${Math.round(progressValue)}%`;
            }

            // Обновление статистики
            function updateStats() {
                completedCount.textContent = questionsAnswered;
                correctCount.textContent = correctAnswers.toFixed(1);
                uniqueTasks.textContent = usedQuestionIds.size;
            }

            // Таймер
            function startTimer() {
                updateTimerDisplay();
                timerInterval = setInterval(function() {
                    timeLeft--;
                    updateTimerDisplay();
                    
                    if (timeLeft <= 0) {
                        clearInterval(timerInterval);
                        timeUp();
                    }
                }, 1000);
            }

            // Обновление отображения таймера
            function updateTimerDisplay() {
                const minutes = Math.floor(timeLeft / 60);
                const seconds = timeLeft % 60;
                timer.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                // Изменение цвета при малом остатке времени
                if (timeLeft <= 30) {
                    timer.className = 'timer danger';
                } else if (timeLeft <= 60) {
                    timer.className = 'timer warning';
                } else {
                    timer.className = 'timer';
                }
            }

            // Сброс таймера
            function resetTimer() {
                clearInterval(timerInterval);
                timeLeft = 180;
                startTimer();
            }

            // Время вышло
            function timeUp() {
                feedback.textContent = 'Время вышло! Попробуйте быстрее.';
                feedback.className = 'feedback incorrect';
                feedback.style.display = 'block';
                character.className = 'character sad';
                characterMessage.textContent = 'Время вышло! В следующий раз будь быстрее!';
                checkBtn.disabled = true;
                hintBtn.disabled = true;
                nextBtn.disabled = false;
            }

            // Запуск приложения
            init();
        });
    </script>
</body>
</html>
