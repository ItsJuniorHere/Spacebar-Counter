# Spacebar-Counter
Basically, you just click spacebar and you count it and I prefer click for 1 minute on your spacebar really quick with your friends and when the times up, you can see who got the fastest one. 

  <div id="activity">
  <h1 id="counter">You have hit the spacebar <span class="hits">0</span> times.</h1>
  <a href="#" onclick="resetHits()" class="tryagain">RESTART</a>
		</div>

  var hits = 0;
var hitElement = document.querySelector( '.hits' );
document.body.onkeyup = function(e) {
  if( e.keyCode == 32 ) {
    addHit();
  }
}

var addHit = function() {
  hits++;
  renderHits();
}

var renderHits = function() {
  hitElement.innerHTML = hits;
}

var resetHits = function() {
  hits = 1;
  renderHits();
  }
