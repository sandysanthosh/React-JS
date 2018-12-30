# React-JS
RXJS react Library


<!DOCTYPE html> 
<html>  
<head>  
  <meta  charset="utf-8">   
  <meta name="viewport" content="width=device-width">     
  <title>bufferCount</title>  
  <script src="https://npmcdn.com/@reactivex/rxjs@5.0.0-beta.3/dist/global/Rx.umd.js"></script>
</head> 
<body>  
    <button>click me!</button>  
    </body> 
  <script type="text/javascript"> 
var button = document.querySelector('button');  
Rx.Observable.fromEvent(button, 'click')  
  .throttleTime(1000) 
  .map(event => event.clientX)  
  .scan((count, clientX) => count + clientX, 0) 
  .subscribe(count => console.log(count));  
    </script>   
</html> 
