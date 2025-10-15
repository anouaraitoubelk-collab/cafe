<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Café Express</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2ebe3;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      text-align: center;
      width: 300px;
    }
    h1 {
      color: #5c3a21;
    }
    select, button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    button {
      background: #5c3a21;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #754b2f;
    }
    .message {
      margin-top: 15px;
      color: rgb(100, 0, 128);
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>☕ Café Express</h1>
    <label for="coffee">Choisissez votre café :</label>
    <select id="coffee">
      <option value="Espresso">Espresso</option>
      <option value="Cappuccino">Cappuccino</option>
      <option value="Latte">Latte</option>
      <option value="Americano">Americano</option>
      <option value="Thé">Thé</option>
    </select>
    <button onclick="commander()">Commander</button>
    <div class="message" id="message"></div>
  </div>

  <script>
    function commander() {
      const choix = document.getElementById("coffee").value;
      const msg = document.getElementById("message");
      msg.textContent = `☕ Votre ${choix} est en préparation...`;
      setTimeout(() => {
        msg.textContent = `✅ Votre ${choix} est prêt ! Bon dégustation 😋`;
      }, 2000);
    }
  </script>
</body>
</html>
