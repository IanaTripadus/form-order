<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8">
  <title>Замовлення</title>
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
  <script>
    (function() {
      emailjs.init("jWEEV_Yjyi29yFvSu"); // ← твій публічний ключ
    })();

    function sendEmail(e) {
      e.preventDefault();

      emailjs.sendForm('service_qbp63a9', 'template_3o3wrsm', e.target)
        .then(function(response) {
          console.log('✅ Відправлено!', response.status, response.text);
          window.location.href = "https://github.com/IanaTripadus"; // редирект
        }, function(error) {
          console.log('❌ Помилка...', error);
          alert("Щось пішло не так. Спробуйте ще раз.");
        });
    }
  </script>
  <style>
    body {
      font-family: sans-serif;
      background: #f8f8f8;
      padding: 20px;
    }
    .container {
      max-width: 500px;
      margin: 0 auto;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    input, textarea {
      width: 100%;
      padding: 12px;
      margin-bottom: 20px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    button {
      width: 100%;
      padding: 15px;
      background: black;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
    }
    button:hover {
      background: #333;
    }
  </style>
</head>
<body>
  <form class="container" onsubmit="sendEmail(event)">
    <h2>Залишити замовлення</h2>
    <input type="text" name="user_name" placeholder="Ваше ім’я" required>
    <input type="email" name="user_email" placeholder="Email" required>
    <textarea name="message" rows="5" placeholder="Повідомлення" required></textarea>
    <button type="submit">Замовити</button>
  </form>
</body>
</html>

GitHub (https://github.com/IanaTripadus)
IanaTripadus - Overview
GitHub is where IanaTripadus builds software.
