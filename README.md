# Project- Temprature converter

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Temperature Converter</title>


<style>
  body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-image: url('PT.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    min-height: 110vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .container {
    background-color: rgba(252, 252, 252, 0.8);
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    text-align: center;
  }
</style>


</head>
<body>
<div class="container">
  <h1>Temperature Converter</h1><br>
  <label for="celsius">Enter Temperature in Celsius:</label>
  <input type="number" id="celsius" placeholder="Enter Celsius temperature" step="0.1">
  <button onclick="convertTemperature()">Convert</button>
  <p id="result"></p>
</div>


<script>
  function convertTemperature() {
    const celsiusInput = document.getElementById('celsius');
    const resultElement = document.getElementById('result');
    
    if (celsiusInput.value === '') {
      resultElement.textContent = 'Please enter a temperature.';
      return;
    }
    
    const celsius = parseFloat(celsiusInput.value);
    const fahrenheit = (celsius * 9/5) + 32;
    
    resultElement.textContent = `${celsius.toFixed(1)}°C is ${fahrenheit.toFixed(1)}°F`;
  }
</script>
</body>
</html>
