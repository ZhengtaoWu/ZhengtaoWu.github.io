# Personal Website of Zhengtao Wu

## About me

I'm a college student from [South China University of Technology](https://www.scut.edu.cn/) major in biomedical engineering. My second year of college starts in September, 2022. 

## Gallery (update from time to time)

### Leica X2

![Gramma](L9980422.JPG)

![Deliver Guys](L9980417.JPG)

### Nikon Z5 with 24-50mm f4-6.3

## Photos collections

## Contact me

  * Email: zt-wu@outlook.com
  * QQ: 1127560895
  * [Instagram](https://www.instagram.com/zhengtao_wu/)

<!-- original : https://codepen.io/SeanNorton/pen/LWBXQL -->
<!DOCTYPE html>
<html lang="en">
<head>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Bebas+Neue" rel="stylesheet">

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>greeting2</title>

    <style>

        /*CSS RESETS*/

body{
    background-color: #fff;
    line-height: 1.6;

}

h1 {
    margin-top: 0;
}


/*CSS START*/

.full-table {
    display: table;
    height: 100%;
    width: 100%;
}

.table-cell {
    display: table-cell;
    vertical-align: middle;
    text-align: center;
}

.card {
    padding: 10px 25px 10px 25px;
    border-radius: 10px;
    background: #553c4e;
    width: 85vw;
    color: #fff;
    display: inline-block;
    box-shadow: 2px 2px 1px 0px #330835;
}

.card:hover {
    margin-top: 2px;
    box-shadow: none;
}

.clock {
    display: inline;
    font-family: 'Bebas Neue', cursive;
    font-size: 2em;
   
}

.time {
    display: inline;
    min-width: 37px;
}

.colon {
    font-size: 1.1em;
    display: inline-block;
}

.date {
    display: inline;
    min-width: 162px;
    font-family: 'Bebas Neue', cursive;
    font-size: 2em;
    padding-right: 30px;
}
.greet{
    
    display:inline;
    font-family: 'Dancing Script', cursive;
    font-size: 2rem;
     padding-right: 30px;
}

    </style>
</head>
<body>
    <link href="https://fonts.googleapis.com/css?family=Lobster|Roboto:400,700" rel="stylesheet">

<div class="full-table">
  <div class="table-cell">
    
    <div class="card">
        <div class="greet" id="greet"></div>
      <div class="date" id="date"></div>
      <div class="clock">
        <div class="time" id="hour"></div>
        <div class="colon">:</div>
        <div class="time" id="min"></div>
        <div class="colon">:</div>
        <div class="time" id="sec"></div>
      </div>
    </div>
    
  </div>
</div>

<script>
    function date() {
var today = new Date();
document.getElementById('date').innerHTML = today.toDateString();
}


function clock() {
var today = new Date();
var hour = zeros(twelveHour(today.getHours()));
var minutes = zeros(today.getMinutes());
var seconds = zeros(today.getSeconds());
if(today.getHours() >=12){
    seconds+=" pm"
}
else{
    seconds+=" am"
}
hrs = today.getHours();
if (hrs < 12)
        greet = 'Good Morning  ';
    else if (hrs >= 12 && hrs <= 17)
        greet = 'Good Afternoon ';
    else if (hrs >= 17 && hrs <= 24)
        greet = 'Good Evening  ';
// console.log(today.toLocaleTimeString());
document.getElementById('greet').innerHTML = greet;
document.getElementById('hour').innerHTML = hour;
document.getElementById('min').innerHTML = minutes;
document.getElementById('sec').innerHTML = seconds;
}

function twelveHour(hour) {
if (hour > 12) {
    return hour -= 12 
} else if (hour === 0) {
    return hour = 12;
} else {
    return hour
}
}
    
// adds zero infront of single digit number
function zeros(num) {
if (num < 10) {
    num = '0' + num
};
return num;
}

function dateTime() {
date();
clock();
setTimeout(dateTime, 500);
}

dateTime()
// END
</script>

</body>
</html>
