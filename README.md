
![alt text](countdown_demo3.gif "view a demo for Countdown to Stranger Things Season 2!")
# Countdown to Stranger Things Season 2

## Credit
* Font credit | Jason Kottke's [Silkscreen](http://www.kottke.org/plus/type/silkscreen/index.html)

## Programming Languages used
* JavaScript
* HTML
* CSS

## MVP (Minimum Viable Product)
* Timer counts down to October 27, 2017

## Code Snippets
```
function updateTimer() {

	// Subtract end date from now
	var now = new Date();
	var timeRemaining = endDate.getTime() - now.getTime(); // get miliseconds
	// console.log(timeRemaining); 
	var seconds = Math.floor((timeRemaining / 1000) % 60); // Get rid of minutes find the seconds
	var minutes = Math.floor((timeRemaining / 1000 / 60) % 60);
	var hours = Math.floor((timeRemaining / (1000 * 60 * 60) % 24));
	var days = Math.floor((timeRemaining / (1000 * 60 * 60 * 24) % 7));
	var weeks = Math.floor(timeRemaining / (1000 * 60 * 60 * 24 * 7));

	document.getElementsByClassName('weeks')[0].innerHTML= weeks;  // returns an array of objects
	document.getElementsByClassName('days')[0].innerHTML = days;
	document.getElementsByClassName('hours')[0].innerHTML = hours;
	document.getElementsByClassName('minutes')[0].innerHTML = minutes;
	document.getElementsByClassName('seconds')[0].innerHTML = seconds;

}

var endDate = new Date("October 27, 2017");
```

