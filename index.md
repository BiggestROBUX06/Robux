<!DOCTYPE html>
<html>
<body style="background-color:powderblue;">

<h1><center>Next Concert in:</center></h1>
<p><font size="2" color="red"><center>Created by Omar Aftab</center></font></p>
<h1>
</body>
</html>
<!-- Display the countdown timer in an element -->
<center><p id="demo"></p></center>

<script>
// Set the date we're counting down to
var countDownDate = new Date("Mar 5, 2020 19:10:25").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in the element with id="demo"
  document.getElementById("demo").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("demo").innerHTML ="Concert Time!";
  }
}, 1000);

</script>
