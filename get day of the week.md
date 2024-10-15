<!DOCTYPE html>
<html>
<head>
  <title>Date of Birth to Day of Week</title>
</head>
<body>
  <h2>welcome to webpage </h2><br><br>
  <label for="dob"> enter your Date of Birth:</label><br><br>
  <input type="date" id="dob"><br><br>
  <button class="custom-button" onclick="getDayOfWeek()">Get Day of Week</button><br><br>
  <h3 id="result"></h3>
  <style>
 body{background-color: darkslategrey; text-align: center; color: white;}
 .custom-button {
      background-color: #3498db;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

  </style>
 

  <script>
    function getDayOfWeek() {
      var dobInput = document.getElementById('dob').value;

      if (dobInput !== '') {
        var dob = new Date(dobInput);
        var days = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
        var dayOfWeek = days[dob.getDay()];

        document.getElementById('result').innerText = 'You were born on a ' + dayOfWeek + '.';
      } else {
        document.getElementById('result').innerText = 'Please enter your date of birth.';
      }
    }
  </script>
</body>
</html>
