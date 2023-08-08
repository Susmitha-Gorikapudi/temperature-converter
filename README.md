# temperature-converter
<!DOCTYPE html>
<html>
<head>
  <title>Temperature Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }

    h1 {
      text-align: center;
    }

    .container {
      width: 250px;
      margin: 0 auto;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
    }

 .form-group input {
      width: 100%;
      padding: 10px;
    }

    .fa{
      width: 100%;
      padding: 10px;
      background-color: #87CEEB;
      color: #000000;
      border: none;
      cursor: pointer;
    }

    .res {
      text-align: center;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Temperature Converter</h1>
  <div class="container">
    <div class="form-group">
      <label for="celsius">Celsius</label>
 <input type="number" id="celsius" placeholder="Enter temperature in Celsius" />
    </div>
    <div class="form-group">
      <label for="fahrenheit">Fahrenheit</label>
      <input type="number" id="fahrenheit" placeholder="Enter temperature in Fahrenheit" />
    </div>
    <button class="fa" onclick="convertToCelsius()">Convert to Celsius</button>
    <div>
    <script>
    function convertToCelsius() {
      var fahrenheitInput = document.getElementById("fahrenheit");
      var celsiusResult = document.getElementById("result");
      var fahrenheit = parseFloat(fahrenheitInput.value);
      var celsius = (fahrenheit - 32) * 5 / 9;
      celsiusResult.textContent = fahrenheit + "°F is " + celsius.toFixed(2) + "°C";
    }</script></div>
    
    <button class="fa" onclick="convertToFahrenheit()">Convert to Fahrenheit</button>
    
  

  <div>

<script>
    function convertToFahrenheit() {
      var celsiusInput = document.getElementById("celsius");
      var fahrenheitResult = document.getElementById("result");
      var celsius = parseFloat(celsiusInput.value);
      var fahrenheit = (celsius * 9 / 5) + 32;
      fahrenheitResult.textContent = celsius + "°C is " + fahrenheit.toFixed(2) + "°F";
 }
  </script>
</div>
</div><div class="res" id="result"></div>
</body>
</html>
