<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Live Character Counter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    textarea {
      width: 400px;
      height: 150px;
      font-size: 16px;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      outline: none;
    }
    textarea:focus {
      border-color: #007BFF;
      box-shadow: 0 0 4px rgba(0,123,255,0.4);
    }
    .counter {
      margin-top: 8px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>

  <h2>Live Character Counter</h2>
  <textarea id="textInput" placeholder="Type your text here..."></textarea>
  <div class="counter">Characters: <span id="charCount">0</span></div>

  <script>
    const textarea = document.getElementById("textInput");
    const charCount = document.getElementById("charCount");

    textarea.addEventListener("input", () => {
      charCount.textContent = textarea.value.length;
    });
  </script>

</body>
</html>
