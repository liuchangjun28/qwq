<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
	</head>
	<body>
		<a href="https://www.bilibili.com/video/BV1fz4y1Q7Zh/"><h1 align="center">“只愿君心似我心，定不负相思意，我爱岳楦。”</h1></a>
		<a href="https://www.bilibili.com/video/BV1U3411L725/"><h1 align="center"><canvas id="c"></canvas>
		<h1 align="center"><canvas id="c"></canvas>    
			<script>    
		   		var b = document.body;
		    	var c = document.getElementsByTagName('canvas')[0];
		    	var a = c.getContext('2d');
			</script>
		    <script>
			eval('var M=Math,n=M.pow,i,E=2,F="rgba(233,61,109,",d=M.cos,z=M.sin,L=1,u=30,W=window,w=c.width=W.innerWidth,h=c.height=W.innerHeight,r=_1){return M.random()*2-1},y="px Arial",v="爱你",q="♥",X=w/2,Y=h/2,T=4,p=_1){var e=this;e.g=_1){e.x=X;e.y=Y;e.k=0;e.l=0;e.t=M.random()*19000;e.c=e.t};e.d=_1){a.fillStyle=F+(e.c/e.t)+")";a.fillText(q,e.x,e.y);e.c-=50;e.x+=e.k;e.y+=e.l;e.k=e.k+r();e.l=e.l+r();if(e.c<0||e.x>w||e.x<0||e.y>h||e.y<0){e.g()}};e.g()},A,B;a.textAlign="center";a.strokeStyle="#000";a.lineWidth=2;for(i=0;i<350;i++){M[i]=new p()}setInterval(_1){a.clearRect(0,0,w,h);a.font=u+y;X=(w/6*n(z(T),3)+w/2);Y=0.8*(-h/40*(13*d(T)-5*d(2*T)-2*d(3*T)-d(4*T))+h/2.3);T+=(z(T)+3)/99;for(i=0;i<350;i++){with(M[i]){A=(x/w-0.5)*2,B=-(y/h-0.5);if(L&&(A*A+2*n((B-0.5*n(M.abs(A),0.5)),2))>0.11){k=l=0}d()}}a.font=120+y;if(E>0.1){if(E<1){a.fillStyle=F+E+")";a.fillText("Click",w/2,h/2)}E-=0.02}a.fillStyle="#E93D6D";a.fillText(v,X,Y+u);a.strokeText(v,X,Y+u)},50);b.bgColor="#FFEFF2";c.οnmοuseup=_1){L=(L)?0:1}'.replace(/(_1)/g,'function('))
		    </script></h1>
		<ul>
					<a href="https://www.bilibili.com/video/BV1m64y167dd/"><li><h1 align="center">愿我如星君如月，夜夜流光相皎洁</h1></li></a>
					<a href="https://www.bilibili.com/video/BV1GM4y1M792/"><li><h1 align="center">天不老，情难绝。心似双丝网，中有千千结。</h1></li></a>
				           <ul>
							   
					        
		<ul>
								  
			
								  </ul>
								  <a href="https://www.bilibili.com/video/BV1bW4116756/">
		<h1 align="center"><div class="container" onselectstart="return false;" unselectable="on" style="-moz-user-select:none;">
			
			    <div class="body_left">
			        <img src="images/biubiubiu.gif" alt="" ondragstart='return false;'>
			    </div>
			
			    <div class="body_center love">
			        <div class="block">
			            <div class="div1"></div>
			            <div class="div2"></div>
			            <div class="div3"></div>
			            <div class="div4"></div>
			        </div>
			    </div>
			
			</div>
			
			<div class="footer">
			    <div class="border">
			        <div class="border-top"></div>
			        <div class="border-bottom"></div>
			    </div>
			
			</div>
		  </style>
		 </HEAD>
		
		 <BODY>
		  <canvas id="pinkboard"></canvas>
		  <script>
		  /*
		 * Settings
		 */
		var settings = {
		  particles: {
		    length:   500, // maximum amount of particles
		    duration:   2, // particle duration in sec
		    velocity: 100, // particle velocity in pixels/sec
		    effect: -0.75, // play with this for a nice effect
		    size:      30, // particle size in pixels
		  },
		};
		
	/*
	 * RequestAnimationFrame polyfill by Erik Möller
	 */
	(function(){var b=0;var c=["ms","moz","webkit","o"];for(var a=0;a<c.length&&!window.requestAnimationFrame;++a){window.requestAnimationFrame=window[c[a]+"RequestAnimationFrame"];window.cancelAnimationFrame=window[c[a]+"CancelAnimationFrame"]||window[c[a]+"CancelRequestAnimationFrame"]}if(!window.requestAnimationFrame){window.requestAnimationFrame=function(h,e){var d=new Date().getTime();var f=Math.max(0,16-(d-b));var g=window.setTimeout(function(){h(d+f)},f);b=d+f;return g}}if(!window.cancelAnimationFrame){window.cancelAnimationFrame=function(d){clearTimeout(d)}}}());
	
	/*
	 * Point class
	 */
	var Point = (function() {
	  function Point(x, y) {
	    this.x = (typeof x !== 'undefined') ? x : 0;
	    this.y = (typeof y !== 'undefined') ? y : 0;
	  }
	  Point.prototype.clone = function() {
	    return new Point(this.x, this.y);
	  };
	  Point.prototype.length = function(length) {
	    if (typeof length == 'undefined')
	      return Math.sqrt(this.x * this.x + this.y * this.y);
	    this.normalize();
	    this.x *= length;
	    this.y *= length;
	    return this;
	  };
	  Point.prototype.normalize = function() {
	    var length = this.length();
	    this.x /= length;
	    this.y /= length;
	    return this;
	  };
	  return Point;
	})();
	
	/*
	 * Particle class
	 */
	var Particle = (function() {
	  function Particle() {
	    this.position = new Point();
	    this.velocity = new Point();
	    this.acceleration = new Point();
	    this.age = 0;
	  }
	  Particle.prototype.initialize = function(x, y, dx, dy) {
	    this.position.x = x;
	    this.position.y = y;
	    this.velocity.x = dx;
	    this.velocity.y = dy;
	    this.acceleration.x = dx * settings.particles.effect;
	    this.acceleration.y = dy * settings.particles.effect;
	    this.age = 0;
	  };
	  Particle.prototype.update = function(deltaTime) {
	    this.position.x += this.velocity.x * deltaTime;
	    this.position.y += this.velocity.y * deltaTime;
	    this.velocity.x += this.acceleration.x * deltaTime;
	    this.velocity.y += this.acceleration.y * deltaTime;
	    this.age += deltaTime;
	  };
	  Particle.prototype.draw = function(context, image) {
	    function ease(t) {
	      return (--t) * t * t + 1;
	    }
	    var size = image.width * ease(this.age / settings.particles.duration);
	    context.globalAlpha = 1 - this.age / settings.particles.duration;
	    context.drawImage(image, this.position.x - size / 2, this.position.y - size / 2, size, size);
	  };
	  return Particle;
	})();
	
	/*
	 * ParticlePool class
	 */
	var ParticlePool = (function() {
	  var particles,
	      firstActive = 0,
	      firstFree   = 0,
	      duration    = settings.particles.duration;
	  
	  function ParticlePool(length) {
	    // create and populate particle pool
	    particles = new Array(length);
	    for (var i = 0; i < particles.length; i++)
	      particles[i] = new Particle();
	  }
	  ParticlePool.prototype.add = function(x, y, dx, dy) {
	    particles[firstFree].initialize(x, y, dx, dy);
	    
	    // handle circular queue
	    firstFree++;
	    if (firstFree   == particles.length) firstFree   = 0;
	    if (firstActive == firstFree       ) firstActive++;
	    if (firstActive == particles.length) firstActive = 0;
	  };
	  ParticlePool.prototype.update = function(deltaTime) {
	    var i;
	    
	    // update active particles
	    if (firstActive < firstFree) {
	      for (i = firstActive; i < firstFree; i++)
	        particles[i].update(deltaTime);
	    }
	    if (firstFree < firstActive) {
	      for (i = firstActive; i < particles.length; i++)
	        particles[i].update(deltaTime);
	      for (i = 0; i < firstFree; i++)
	        particles[i].update(deltaTime);
	    }
	    
	    // remove inactive particles
	    while (particles[firstActive].age >= duration && firstActive != firstFree) {
	      firstActive++;
	      if (firstActive == particles.length) firstActive = 0;
	    }
	    
	    
	  };
	  ParticlePool.prototype.draw = function(context, image) {
	    // draw active particles
	    if (firstActive < firstFree) {
	      for (i = firstActive; i < firstFree; i++)
	        particles[i].draw(context, image);
	    }
	    if (firstFree < firstActive) {
	      for (i = firstActive; i < particles.length; i++)
	        particles[i].draw(context, image);
	      for (i = 0; i < firstFree; i++)
	        particles[i].draw(context, image);
	    }
	  };
	  return ParticlePool;
	})();
	
	/*
	 * Putting it all together
	 */
	(function(canvas) {
	  var context = canvas.getContext('2d'),
	      particles = new ParticlePool(settings.particles.length),
	      particleRate = settings.particles.length / settings.particles.duration, // particles/sec
	      time;
	  
	  // get point on heart with -PI <= t <= PI
	  function pointOnHeart(t) {
	    return new Point(
	      160 * Math.pow(Math.sin(t), 3),
	      130 * Math.cos(t) - 50 * Math.cos(2 * t) - 20 * Math.cos(3 * t) - 10 * Math.cos(4 * t) + 25
	    );
	  }
	  
	  // creating the particle image using a dummy canvas
	  var image = (function() {
	    var canvas  = document.createElement('canvas'),
	        context = canvas.getContext('2d');
	    canvas.width  = settings.particles.size;
	    canvas.height = settings.particles.size;
	    // helper function to create the path
	    function to(t) {
	      var point = pointOnHeart(t);
	      point.x = settings.particles.size / 2 + point.x * settings.particles.size / 350;
	      point.y = settings.particles.size / 2 - point.y * settings.particles.size / 350;
	      return point;
	    }
	    // create the path
	    context.beginPath();
	    var t = -Math.PI;
	    var point = to(t);
	    context.moveTo(point.x, point.y);
	    while (t < Math.PI) {
	      t += 0.01; // baby steps!
	      point = to(t);
	      context.lineTo(point.x, point.y);
	    }
	    context.closePath();
	    // create the fill
	    context.fillStyle = '#ea80b0';
	    context.fill();
	    // create the image
	    var image = new Image();
	    image.src = canvas.toDataURL();
	    return image;
	  })();
	  
	  // render that thing!
	  function render() {
	    // next animation frame
	    requestAnimationFrame(render);
	    
	    // update time
	    var newTime   = new Date().getTime() / 1000,
	        deltaTime = newTime - (time || newTime);
	    time = newTime;
	    
	    // clear canvas
	    context.clearRect(0, 0, canvas.width, canvas.height);
	    
	    // create new particles
	    var amount = particleRate * deltaTime;
	    for (var i = 0; i < amount; i++) {
	      var pos = pointOnHeart(Math.PI - 2 * Math.PI * Math.random());
	      var dir = pos.clone().length(settings.particles.velocity);
	      particles.add(canvas.width / 2 + pos.x, canvas.height / 2 - pos.y, dir.x, -dir.y);
	    }
	    
	    // update and draw particles
	    particles.update(deltaTime);
	    particles.draw(context, image);
	  }
	  
	  // handle (re-)sizing of the canvas
	  function onResize() {
	    canvas.width  = canvas.clientWidth;
	    canvas.height = canvas.clientHeight;
	  }
	  window.onresize = onResize;
	  
	  // delay rendering bootstrap
	  setTimeout(function() {
	    onResize();
	    render();
	  }, 10);
	})(document.getElementById('pinkboard'));
	  </script></h1></br>
	<h1 align="center"><a href="https://www.bilibili.com/video/BV1Fm4y1o7Z8/">【点击可见深情告白】</a></h1></br>
		  <a href="https://www.bilibili.com/video/BV13Q4y1i7nm/"><h1 align="center">生当复来归，死当长相思</h1></a>
		  <a href="https://www.bilibili.com/video/BV16t4y1576B/"><h1 align="center"><img src="js/IMG_20221029_121934.jpg" alt=""></h1>
		  <a href="https://www.bilibili.com/video/BV1FF411G7Ax/"><h1 align="center"><img src="js/cc.jpg" alt=""></h1></br>
		<a href="https://www.bilibili.com/video/BV1GS4y1N79e/"><h1 align="center"><img src="js/ca.jpg" alt=""></h1>
		</br>
		
		<a href="https://www.bilibili.com/video/BV1ZR4y1s75N/"><h1 align="center"><img src="js/gf.jpg" alt=""></h1>
	</body>
</html>


