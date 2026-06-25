<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maestro Method | Практический разбор</title>
    <style>
        /* Оставляем наши ультра-легкие стили */
        body {
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #0b1d12;
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            text-align: center;
        }
        .container {
            max-width: 540px;
            padding: 20px;
            box-sizing: border-box;
        }
        .надзаголовок {
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #a8c3b0;
            margin-bottom: 15px;
        }
        h1 {
            font-size: 26px;
            line-height: 1.3;
            margin: 0 0 15px 0;
            font-weight: 700;
        }
        .описание {
            font-size: 16px;
            line-height: 1.5;
            color: #d1e0d7;
            margin-bottom: 30px;
        }
        .btn {
            background-color: #ffffff;
            color: #0b1d12;
            border: none;
            padding: 16px 32px;
            font-size: 16px;
            font-weight: 700;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
            box-sizing: border-box;
            transition: background 0.2s;
        }
        .btn:hover {
            background-color: #e2ede6;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="надзаголовок">Бесплатное практическое обучение</div>
        <h1>Как экспертам получать стабильные заявки и продажи онлайн без хаоса и рутины</h1>
        <div class="описание">Практический разбор методологии и структуры ведения экспертной онлайн-практики для коучей и консультантов.</div>
        
        <button class="btn" id="start-btn" onclick="loadSendPulsePopup()">ПОЛУЧИТЬ ДОСТУП К ОБУЧЕНИЮ</button>
    </div>

    <script>
        function loadSendPulsePopup() {
            // Меняем текст на кнопке, пока подгружается попап, чтобы пользователь видел отклик
            var btn = document.getElementById('start-btn');
            btn.innerText = 'ЗАГРУЗКА...';
            btn.disabled = true;

            // Динамически и мгновенно создаем и внедряем скрипт SendPulse в момент клика
            var script = document.createElement('script');
            script.async = true;
            script.src = "https://static.sppopups.com/assets/loader.js";
            script.setAttribute('data-chats-widget-id', '74f12016-b7a4-48b5-85ad-a041d59361cb');
            
            // Как только скрипт загрузился, возвращаем кнопке исходный вид
            script.onload = function() {
                btn.innerText = 'ПОЛУЧИТЬ ДОСТУП К ОБУЧЕНИЮ';
                btn.disabled = false;
                
                // Инструкция для SendPulse автоматически открыть попап, если он настроен на клик или показ
                if (window.spPopups) {
                    window.spPopups.open(); 
                }
            };

            document.head.appendChild(script);
        }
    </script>

</body>
</html>
