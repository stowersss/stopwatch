<html>
<head><style>#time {font-size: 48px;}</style></head>
<button onclick="go()">Go</button>
<div id="time"></div>

<script>
	
var min = 0;	
var sec = 0;
var timeos = document.getElementById('time');


function go() {
	setInterval(timer, 1000);
}

function timer() {
	if(sec > 58) {
		min++;
		sec = -1;
	}
	sec++;
	if(min >= 10 && sec > 9) {
		timeos.textContent = + min + ":" + sec;
	} else if(min >= 10 && sec < 10) {
		timeos.textContent = min + ":" + "0" + sec;
	} else if(sec < 10) {
		timeos.textContent = "0" + min + ":" + "0" + sec;
	} else {
	timeos.textContent ="0" + min + ":" + sec;
}

console.log("Minutes: " + min +" Seconds: " + sec);
}
</script>
</html>
