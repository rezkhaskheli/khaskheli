<!DOCTYPE html>
<html>
<head>
  <title>Even Odd Finder</title>
   <!-- Bootstrap CSS -->
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
   <style>
     .body{
      height: 500px;
      background-color: gray;
    }
</style>
  </head>
<body>
  <div class="container bg-primary">
    <div class="row">
        <div class="col-sm-2">
          <h3>My Projects</h3>
        </div>
        <div class="col-sm-10">
          <a href="/index.html"><button type="button" class="btn btn-info">Home</button></a>
          <a href="/EvenOdd.html"><button type="button" class="btn btn-warning">Even Odd Finder</button></a>
          <a href="/Tablegenerator.html"><button type="button" class="btn btn-secondary">Table Generator</button></a>
          <a href="/Factorial.html"><button type="button" class="btn btn-success">Factorial</button></a>
          <a href="/Primenumber.html"><button type="button" class="btn btn-danger">Prime Number</button></a>
          <a href="/currencyconverter.html"><button type="button" class="btn btn-info">Currency Converter</button></a>
          <a href="/Marksheet.html"><button type="button" class="btn btn-warning">Marksheet</button></a>
      </div>
    </div>
</div>
<div class="container body">
  <div class="row">
    <div class="col">
      <h2>Currency Converter</h2>

  <label>Amount:</label>
  <input type="number" id="amount" placeholder="Enter amount" />

  <label>From:</label>
  <select id="from">
    <option value="USD">USD</option>
    <option value="SAR">SAR</option>
    <option value="AED">AED</option>
    <option value="EURO">EURO</option>
    <option value="PKR">PKR</option>
  </select>

  <label>To:</label>
  <select id="to">
    <option value="USD">USD</option>
    <option value="SAR">SAR</option>
    <option value="AED">AED</option>
    <option value="EURO">EURO</option>
    <option value="PKR">PKR</option>
  </select>

  <button id="convert">Convert</button>

  <h3 id="result"></h3>

  <script>
    // Fixed exchange rates (example values, not real-time)
    const rates = {
      USD: { USD: 1, SAR: 3.75, AED: 3.67, EURO: 0.92, PKR: 278 },
      SAR: { USD: 0.27, SAR: 1, AED: 0.98, EURO: 0.25, PKR: 74 },
      AED: { USD: 0.27, SAR: 1.02, AED: 1, EURO: 0.25, PKR: 75 },
      EURO: { USD: 1.09, SAR: 4.10, AED: 4.05, EURO: 1, PKR: 302 },
      PKR: { USD: 0.0036, SAR: 0.013, AED: 0.013, EURO: 0.0033, PKR: 1 },
    };

    document.querySelector("#convert").addEventListener("click", () => {
      const amount = parseFloat(document.querySelector("#amount").value);
      const from = document.querySelector("#from").value;
      const to = document.querySelector("#to").value;
      const resultField = document.querySelector("#result");

      if (isNaN(amount) || amount <= 0) {
        resultField.textContent = "Please enter a valid amount.";
        return;
      }

      const rate = rates[from][to];
      const converted = amount * rate;

      resultField.textContent = `${amount} ${from} = ${converted.toFixed(2)} ${to}`;
    });
  </script>
    </div>
  </div>
</div>
<div class="container mtop bg-primary text-white">
  <div class="row">
      <div class="col">
          <marquee behavior="" direction="">Project By: Riaz Ahmed - Batch - 49 - UI Learning - Gulshan-e-Iqbal</marquee>
      </div>
  </div>
</div>
</body>
</html>
