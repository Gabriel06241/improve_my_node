# var arrcadena = ["02:35","01:15","02:25","01:35"];

var hoursInSeconds = 0;
var minutesInSeconds = 0;
for(var i=0; i<arrcadena.length; ++i){
  var SplitCadena = arrcadena[i].split(':');
  hoursInSeconds = hoursInSeconds + (SplitCadena[0]*3600);
  minutesInSeconds = minutesInSeconds + (SplitCadena[1]*60);
}

var hours = parseInt((hoursInSeconds+minutesInSeconds)/3600);
var minutes = ((hoursInSeconds+minutesInSeconds)%3600)/60;

if (hours<10){
  hours = "0"+hours;
}

console.log(hours+":"+minutes);
