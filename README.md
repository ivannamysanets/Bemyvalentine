<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💘</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #f9c5d1, #fddde6);
      font-family: "Segoe UI", sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .card {
      background: white;
      padding: 30px 25px 40px;
      border-radius: 24px;
      text-align: center;
      width: 320px;
      position: relative;
      box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    }

    .cat {
      font-size: 64px;
      margin-bottom: 10px;
    }

    h2 {
      margin: 10px 0 25px;
      font-weight: 600;
    }

    .buttons {
      position: relative;
      height: 120px;
    }

    button {
      border: none;
      padding: 12px 26px;
      border-radius: 30px;
      font-size: 16px;
      cursor: pointer;
    }

    #yes {
      background: #ff4d79;
      color: white;
    }

    #no {
      background: #eee;
      position: absolute;
      left: 120px;
      top: 60px;
    }

    .hint {
      margin-top: 20px;
      font-size: 13px;
      color: #777;
    }

    .final {
      display: none;
      font-size: 22px;
    }
  </style>
</head>
<body>
  <div class="card" id="card">
    <div class="cat">🐱💗</div>
    <h2>Will you be my Valentine?</h2>

    <div class="buttons">
      <button id="yes">Yes</button>
      <button id="no">No</button>
    </div>

    <div class="hint">“No” seems a bit shy 😈</div>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const card = document.getElementById("card");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 120 - 60;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    yesBtn.addEventListener("click", () => {
      card.innerHTML = `
        <div class="cat">🥰💘</div>
        <div class="final">
          I knew it 💖<br><br>
          Happy Valentine’s Day 😌
        </div>
      `;
    });
  </script>
</body>
</html>
