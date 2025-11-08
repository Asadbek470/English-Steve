# English-Steve
English
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Английский с Стивом | Понятные задания</title>
    <style>
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
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        #check-btn {
            background: linear-gradient(135deg, #58cc02, #4cb400);
            color: white;
        }

        #check-btn:hover {
            background: linear-gradient(135deg, #4cb400, #3a9c00);
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

        #check-btn:disabled, #next-btn:disabled, #pause-btn:disabled {
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

        .certificate-section {
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            text-align: center;
            display: none;
        }

        .certificate {
            border: 5px solid #58cc02;
            padding: 30px;
            margin: 20px auto;
            max-width: 600px;
            background-color: #f9f9f9;
            position: relative;
        }

        .certificate h2 {
            color: #4cb400;
            margin-bottom: 20px;
        }

        .certificate p {
            margin-bottom: 15px;
            font-size: 18px;
        }

        .certificate .level {
            font-size: 24px;
            font-weight: bold;
            color: #58cc02;
            margin: 20px 0;
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

        /* Стили для модального окна словаря */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }

        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 20px;
            border-radius: 15px;
            width: 90%;
            max-width: 800px;
            max-height: 80vh;
            overflow-y: auto;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover {
            color: #000;
        }

        .dictionary-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .dictionary-title {
            color: #4cb400;
            font-size: 24px;
        }

        .alphabet-nav {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
            margin-bottom: 20px;
            justify-content: center;
        }

        .alphabet-letter {
            padding: 5px 10px;
            background-color: #f0f2f5;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .alphabet-letter:hover {
            background-color: #e8f5e8;
        }

        .alphabet-letter.active {
            background-color: #58cc02;
            color: white;
        }

        .word-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
        }

        .word-card {
            background-color: #f9f9f9;
            border-radius: 8px;
            padding: 15px;
            border-left: 4px solid #58cc02;
        }

        .word-english {
            font-weight: bold;
            font-size: 18px;
            margin-bottom: 5px;
        }

        .word-russian {
            color: #666;
        }

        .pause-overlay {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            justify-content: center;
            align-items: center;
        }

        .pause-content {
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            max-width: 500px;
            width: 90%;
        }

        .pause-title {
            color: #ff9500;
            font-size: 24px;
            margin-bottom: 15px;
        }

        .pause-message {
            margin-bottom: 20px;
            font-size: 16px;
        }

        .pause-timer {
            font-size: 36px;
            font-weight: bold;
            color: #ff3b30;
            margin: 15px 0;
        }

        /* Стили для выбора уровня */
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
            
            .word-list {
                grid-template-columns: 1fr;
            }
            
            .header-buttons {
                flex-direction: column;
                gap: 5px;
            }
            
            .level-grid {
                grid-template-columns: 1fr;
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
                    <button class="header-btn" id="dictionary-btn">Словарь</button>
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
                    <p>~60 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="A2">
                    <h3>A2 (Элементарный)</h3>
                    <p>Простые повседневные ситуации</p>
                    <p>~70 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B1">
                    <h3>B1 (Средний)</h3>
                    <p>Общение на знакомые темы</p>
                    <p>~100 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B1+">
                    <h3>B1+ (Средний+)</h3>
                    <p>Более сложные грамматические конструкции</p>
                    <p>~110 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="B2">
                    <h3>B2 (Выше среднего)</h3>
                    <p>Сложные тексты и абстрактные темы</p>
                    <p>~130 уникальных заданий</p>
                </div>
                <div class="level-card" data-level="C1">
                    <h3>C1 (Продвинутый)</h3>
                    <p>Свободное владение языком</p>
                    <p>~160 уникальных заданий</p>
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
                <h2>Поздравляем!</h2>
                <p>Вы успешно завершили уровень <span id="certificate-level-name">A1</span>!</p>
                <div class="certificate">
                    <h2>Сертификат об окончании</h2>
                    <p>Настоящим удостоверяется, что</p>
                    <p><strong>Ученик</strong></p>
                    <p>успешно завершил курс</p>
                    <p class="level">Английский язык - Уровень <span id="cert-level-name">A1</span></p>
                    <p>в соответствии с общеевропейскими компетенциями владения иностранным языком</p>
                    <p>Правильных ответов: <span id="certificate-score"></span> из <span id="certificate-total"></span></p>
                    <p>Дата: <span id="certificate-date"></span></p>
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
                        <p>~60 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="A2">
                        <h4>A2</h4>
                        <p>Элементарный</p>
                        <p>~70 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B1">
                        <h4>B1</h4>
                        <p>Средний</p>
                        <p>~100 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B1+">
                        <h4>B1+</h4>
                        <p>Средний+</p>
                        <p>~110 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="B2">
                        <h4>B2</h4>
                        <p>Выше среднего</p>
                        <p>~130 уникальных заданий</p>
                    </div>
                    <div class="level-item" data-level="C1">
                        <h4>C1</h4>
                        <p>Продвинутый</p>
                        <p>~160 уникальных заданий</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Модальное окно словаря -->
    <div id="dictionary-modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <div class="dictionary-header">
                <h2 class="dictionary-title">Словарь английского языка</h2>
            </div>
            <div class="alphabet-nav" id="alphabet-nav">
                <!-- Буквы алфавита будут добавлены через JavaScript -->
            </div>
            <div class="word-list" id="word-list">
                <!-- Слова будут добавлены через JavaScript -->
            </div>
        </div>
    </div>

    <!-- Оверлей паузы -->
    <div id="pause-overlay" class="pause-overlay">
        <div class="pause-content">
            <h2 class="pause-title">Обучение на паузе</h2>
            <p class="pause-message">Вы поставили обучение на паузу. У вас есть 5 дней, чтобы вернуться, иначе прогресс уровня будет аннулирован.</p>
            <div class="pause-timer" id="pause-timer">5:00:00:00</div>
            <p>Осталось до аннулирования прогресса:</p>
            <button id="resume-btn">Продолжить обучение</button>
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
            const dictionaryBtn = document.getElementById('dictionary-btn');
            const dictionaryModal = document.getElementById('dictionary-modal');
            const closeModal = document.querySelector('.close');
            const alphabetNav = document.getElementById('alphabet-nav');
            const wordList = document.getElementById('word-list');
            const pauseBtn = document.getElementById('pause-btn');
            const pauseOverlay = document.getElementById('pause-overlay');
            const pauseTimer = document.getElementById('pause-timer');
            const resumeBtn = document.getElementById('resume-btn');

            // Переменные состояния
            let currentQuestion = 0;
            let selectedOption = null;
            let timerInterval;
            let timeLeft = 180; // 3 минуты в секундах
            let progressValue = 10;
            let questionsAnswered = 0;
            let correctAnswers = 0;
            let usedQuestionIds = new Set();
            let currentLevel = '';
            let questionBank = {};
            let currentTaskType = '';
            let pauseStartTime = null;
            let pauseInterval = null;

            // Банк вопросов для всех уровней с ПОНЯТНЫМИ формулировками
            questionBank = {
                'A1': [
                    {
                        id: 1,
                        type: 'multiple-choice',
                        question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "house" переводится как:',
                        options: ['дом', 'лошадь', 'мышь', 'час'],
                        correct: 0
                    },
                    {
                        id: 2,
                        type: 'multiple-choice',
                        question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола "to be" для подлежащего "I"',
                        content: 'I ___ a student.',
                        options: ['am', 'is', 'are', 'be'],
                        correct: 0
                    },
                    {
                        id: 3,
                        type: 'multiple-choice',
                        question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "book" переводится как:',
                        options: ['книга', 'бокс', 'брать', 'готовить'],
                        correct: 0
                    },
                    {
                        id: 4,
                        type: 'multiple-choice',
                        question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в настоящем времени для подлежащего "she"',
                        content: 'She ___ to school every day.',
                        options: ['go', 'goes', 'going', 'went'],
                        correct: 1
                    },
                    {
                        id: 5,
                        type: 'multiple-choice',
                        question: 'Выберите правильный перевод',
                        explanation: 'Переведите слово с английского на русский',
                        content: 'Слово "water" переводится как:',
                        options: ['вода', 'погода', 'работа', 'слово'],
                        correct: 0
                    },
                    {
                        id: 6,
                        type: 'fill-blank',
                        question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'My name ___ John.',
                        correctAnswer: 'is',
                        hint: 'глагол-связка для третьего лица единственного числа'
                    },
                    {
                        id: 7,
                        type: 'fill-blank',
                        question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола "to be"',
                        content: 'I ___ from Russia.',
                        correctAnswer: 'am',
                        hint: 'глагол-связка для первого лица единственного числа'
                    },
                    {
                        id: 8,
                        type: 'fill-blank',
                        question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму глагола в настоящем времени',
                        content: 'She ___ apples every day.',
                        correctAnswer: 'eats',
                        hint: 'глагол в настоящем времени для третьего лица единственного числа'
                    },
                    {
                        id: 9,
                        type: 'sentence-builder',
                        question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'from / I / am / Russia',
                        correctAnswer: 'I am from Russia'
                    },
                    {
                        id: 10,
                        type: 'sentence-builder',
                        question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'like / I / pizza',
                        correctAnswer: 'I like pizza'
                    }
                ],
                'A1+': [
                    {
                        id: 1,
                        type: 'multiple-choice',
                        question: 'Выберите правильный артикль',
                        explanation: 'Выберите правильный неопределенный артикль',
                        content: 'I have ___ apple.',
                        options: ['an', 'a', 'the', '-'],
                        correct: 0
                    },
                    {
                        id: 2,
                        type: 'multiple-choice',
                        question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в настоящем продолженном времени',
                        content: 'He ___ TV now.',
                        options: ['is watching', 'watches', 'watch', 'watched'],
                        correct: 0
                    },
                    {
                        id: 3,
                        type: 'multiple-choice',
                        question: 'Выберите правильное местоимение',
                        explanation: 'Выберите правильное притяжательное местоимение',
                        content: 'This is ___ book.',
                        options: ['my', 'I', 'me', 'mine'],
                        correct: 0
                    },
                    {
                        id: 4,
                        type: 'fill-blank',
                        question: 'Заполните пропуск',
                        explanation: 'Вставьте правильный предлог места',
                        content: 'The book is ___ the table.',
                        correctAnswer: 'on',
                        hint: 'предлог, обозначающий нахождение на поверхности'
                    },
                    {
                        id: 5,
                        type: 'sentence-builder',
                        question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'is / my / This / book',
                        correctAnswer: 'This is my book'
                    }
                ],
                'A2': [
                    {
                        id: 1,
                        type: 'multiple-choice',
                        question: 'Выберите правильную форму глагола',
                        explanation: 'Выберите правильную форму глагола в прошедшем времени',
                        content: 'I ___ to the cinema yesterday.',
                        options: ['went', 'go', 'going', 'goes'],
                        correct: 0
                    },
                    {
                        id: 2,
                        type: 'multiple-choice',
                        question: 'Выберите правильное слово',
                        explanation: 'Выберите слово, которое лучше всего подходит по контексту',
                        content: 'I am very ___ . I need to sleep.',
                        options: ['tired', 'angry', 'happy', 'hungry'],
                        correct: 0
                    },
                    {
                        id: 3,
                        type: 'fill-blank',
                        question: 'Заполните пропуск',
                        explanation: 'Вставьте правильную форму прилагательного в сравнительной степени',
                        content: 'My brother is ___ than me.',
                        correctAnswer: 'taller',
                        hint: 'сравнительная степень прилагательного "tall"'
                    },
                    {
                        id: 4,
                        type: 'sentence-builder',
                        question: 'Составьте правильное предложение',
                        explanation: 'Расставьте слова в правильном порядке',
                        content: 'never / She / drinks / coffee',
                        correctAnswer: 'She never drinks coffee'
                    }
                ]
                // Для демонстрации добавим только эти уровни
            };

            // Для остальных уровней используем A2 вопросы
            questionBank['B1'] = questionBank['A2'];
            questionBank['B1+'] = questionBank['A2'];
            questionBank['B2'] = questionBank['A2'];
            questionBank['C1'] = questionBank['A2'];

            // Словарь английских слов
            const englishDictionary = [
                { word: "apple", translation: "яблоко" },
                { word: "book", translation: "книга" },
                { word: "cat", translation: "кошка" },
                { word: "dog", translation: "собака" },
                { word: "elephant", translation: "слон" },
                { word: "friend", translation: "друг" },
                { word: "house", translation: "дом" },
                { word: "ice", translation: "лед" },
                { word: "juice", translation: "сок" },
                { word: "king", translation: "король" },
                { word: "lion", translation: "лев" },
                { word: "mother", translation: "мать" },
                { word: "night", translation: "ночь" },
                { word: "orange", translation: "апельсин" },
                { word: "pen", translation: "ручка" },
                { word: "queen", translation: "королева" },
                { word: "red", translation: "красный" },
                { word: "sun", translation: "солнце" },
                { word: "table", translation: "стол" },
                { word: "umbrella", translation: "зонт" },
                { word: "vase", translation: "ваза" },
                { word: "water", translation: "вода" },
                { word: "xylophone", translation: "ксилофон" },
                { word: "yellow", translation: "желтый" },
                { word: "zoo", translation: "зоопарк" }
            ];

            // Инициализация приложения
            function init() {
                // Проверяем, не истекла ли пауза
                checkPauseStatus();
                
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
                initDictionary();
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
                setCertificateDate();
                updateStats();
            }

            // Проверка статуса паузы
            function checkPauseStatus() {
                const pauseData = localStorage.getItem('englishPauseData');
                if (pauseData) {
                    const { startTime, level } = JSON.parse(pauseData);
                    pauseStartTime = startTime;
                    
                    // Проверяем, прошло ли 5 дней
                    const now = new Date().getTime();
                    const fiveDaysInMs = 5 * 24 * 60 * 60 * 1000;
                    
                    if (now - startTime >= fiveDaysInMs) {
                        // Аннулируем уровень
                        resetProgress();
                        localStorage.removeItem('englishPauseData');
                        alert('Уровень аннулирован из-за долгой паузы (5 дней). Прогресс сброшен.');
                    } else {
                        // Показываем оверлей паузы
                        showPauseOverlay();
                    }
                }
            }

            // Показать оверлей паузы
            function showPauseOverlay() {
                pauseOverlay.style.display = 'flex';
                updatePauseTimer();
                
                // Запускаем обновление таймера каждую секунду
                pauseInterval = setInterval(updatePauseTimer, 1000);
                
                // Останавливаем основной таймер
                clearInterval(timerInterval);
            }

            // Скрыть оверлей паузы
            function hidePauseOverlay() {
                pauseOverlay.style.display = 'none';
                clearInterval(pauseInterval);
                
                // Возобновляем основной таймер
                startTimer();
            }

            // Обновить таймер паузы
            function updatePauseTimer() {
                if (!pauseStartTime) return;
                
                const now = new Date().getTime();
                const fiveDaysInMs = 5 * 24 * 60 * 60 * 1000;
                const timeLeft = fiveDaysInMs - (now - pauseStartTime);
                
                if (timeLeft <= 0) {
                    // Аннулируем уровень
                    resetProgress();
                    localStorage.removeItem('englishPauseData');
                    hidePauseOverlay();
                    alert('Уровень аннулирован из-за долгой паузы (5 дней). Прогресс сброшен.');
                    return;
                }
                
                // Конвертируем в дни, часы, минуты, секунды
                const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
                const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
                
                pauseTimer.textContent = `${days}:${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            }

            // Инициализация словаря
            function initDictionary() {
                // Создаем навигацию по алфавиту
                const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('');
                alphabetNav.innerHTML = '';
                
                alphabet.forEach(letter => {
                    const letterElement = document.createElement('div');
                    letterElement.className = 'alphabet-letter';
                    letterElement.textContent = letter;
                    letterElement.addEventListener('click', () => {
                        // Убираем активный класс у всех букв
                        document.querySelectorAll('.alphabet-letter').forEach(el => {
                            el.classList.remove('active');
                        });
                        
                        // Добавляем активный класс к выбранной букве
                        letterElement.classList.add('active');
                        
                        // Показываем слова на эту букву
                        showWordsByLetter(letter);
                    });
                    
                    alphabetNav.appendChild(letterElement);
                });
                
                // По умолчанию показываем слова на A
                showWordsByLetter('A');
            }

            // Показать слова на определенную букву
            function showWordsByLetter(letter) {
                const filteredWords = englishDictionary.filter(word => 
                    word.word.charAt(0).toUpperCase() === letter
                );
                
                wordList.innerHTML = '';
                
                filteredWords.forEach(word => {
                    const wordCard = document.createElement('div');
                    wordCard.className = 'word-card';
                    wordCard.innerHTML = `
                        <div class="word-english">${word.word}</div>
                        <div class="word-russian">${word.translation}</div>
                    `;
                    wordList.appendChild(wordCard);
                });
                
                // Если слов нет, показываем сообщение
                if (filteredWords.length === 0) {
                    wordList.innerHTML = '<p>Слов на букву ' + letter + ' не найдено.</p>';
                }
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

                // Следующий вопрос
                nextBtn.addEventListener('click', nextQuestion);

                // Перезапуск
                restartBtn.addEventListener('click', function() {
                    certificateSection.style.display = 'none';
                    taskSection.style.display = 'block';
                    resetProgress();
                    loadRandomQuestion();
                });

                // Словарь
                dictionaryBtn.addEventListener('click', function() {
                    dictionaryModal.style.display = 'block';
                });

                // Закрытие модального окна словаря
                closeModal.addEventListener('click', function() {
                    dictionaryModal.style.display = 'none';
                });

                // Закрытие модального окна при клике вне его
                window.addEventListener('click', function(e) {
                    if (e.target === dictionaryModal) {
                        dictionaryModal.style.display = 'none';
                    }
                });

                // Пауза
                pauseBtn.addEventListener('click', function() {
                    const startTime = new Date().getTime();
                    const pauseData = {
                        startTime: startTime,
                        level: currentLevel
                    };
                    
                    localStorage.setItem('englishPauseData', JSON.stringify(pauseData));
                    pauseStartTime = startTime;
                    
                    showPauseOverlay();
                });

                // Возобновление обучения
                resumeBtn.addEventListener('click', function() {
                    localStorage.removeItem('englishPauseData');
                    pauseStartTime = null;
                    hidePauseOverlay();
                });
            }

            // Загрузка случайного вопроса
            function loadRandomQuestion() {
                // Если все вопросы использованы, начинаем заново
                if (usedQuestionIds.size >= questionBank[currentLevel].length) {
                    usedQuestionIds.clear();
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
                    correctAnswers++;
                    correctCount.textContent = correctAnswers;
                } else {
                    feedback.textContent = `Неправильно. Правильный ответ: ${getCorrectAnswerText(q)}`;
                    feedback.className = 'feedback incorrect';
                    character.className = 'character sad';
                    characterMessage.textContent = getRandomSadMessage();
                }
                
                feedback.style.display = 'block';
                checkBtn.disabled = true;
                nextBtn.disabled = false;
                
                // Обновляем прогресс
                questionsAnswered++;
                completedCount.textContent = questionsAnswered;
                progressValue = Math.min(100, 10 + (questionsAnswered / 10) * 90); // 10 заданий для завершения уровня
                updateProgress();
                
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
                certificateScore.textContent = correctAnswers;
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

            // Обновление статистика
            function updateStats() {
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
                nextBtn.disabled = false;
            }

            // Запуск приложения
            init();
        });
    </script>
</body>
</html>
