$(document).ready(function()
{
	var canvas = $("canvas");
	var context = canvas.get(0).getContext("2d");
	
	var TimerClass = 
	{
		time: 0,
		interval: undefined,
		
		start: function()
		{
			var self = this;
			this.interval = setInterval(function(){self.tick();}, 1000);
		},
		
		tick: function()
		{
			this.time--;
		},
		
		stop: function()
		{
			clearInterval(this.interval);
		},
		
		reset: function()
		{
			this.time = 0;
		}
	};
	
	var _spriteAnimationClass =
	{
		image: spriteAtlas,
		x: 0,
		y: 0,
		srcX: 0,
		srcY: 0,
		frameWidth: 94,
		frameHeight: 94,
		halfWidth: 0,
		halfHeight: 0,
		framesWide: 0,
		framesHigh: 0,
		imageWidth: 0,
		imageHeight: 0,
		startFrame: 0,
		currentFrame: 0,
		numFrames: 0,
		frameRate: 0,
		loop: true,
		isPlaying: false,
		visible: true,
		rotation: 0,
		alpha: 1,
		timer: undefined,
		
		updateFrameCoords : function()
		{
			this.srcX = ((this.startFrame + this.currentFrame) % this.framesWide) * this.frameWidth;
			this.srcY = Math.floor((this.startFrame + this.currentFrame) / this.framesWide) * this.frameHeight;		
		},
		
		init: function(image, frameWidth, frameHeight, startFrame, numFrames, frameRate)
		{
			this.image = image;
			this.frameWidth = frameWidth;
			this.frameHeight = frameHeight;
			this.framesWide = Math.floor(image.width / frameWidth);
			this.framesHigh = Math.floor(image.height / frameHeight);
			this.imageWidth = image.width;
			this.imageHeight = image.height;
			this.startFrame = startFrame;
			this.numFrames = numFrames;
			this.frameRate = frameRate;
			this.halfWidth = Math.ceil(frameWidth * 0.5);
			this.halfHeight = Math.ceil(frameHeight * 0.5);
			this.updateFrameCoords();
		},
		
		play: function(loop)
		{
			this.isPlaying = true;
			this.loop = loop;
			var self = this;
			this.timer = setTimeout(function(){self.updateAnimation();}, this.frameRate);
		},
		
		stop : function(reset)
		{
			if(this.isPlaying)
			{
				this.isPlaying = false;
				if(reset)
				{
					this.currentFrame = 0;
					updateFrameCoords();
				}
				
				clearTimer(this.timer);
			}
		},
		
		updateAnimation: function()
		{
			this.currentFrame++;
			if(this.currentFrame >= this.numFrames)
			{
				if(this.loop)
				{
					this.currentFrame = 0;
				}
				else
				{
					this.isPlaying = false;
					this.currentFrame--;
				}
			}
			this.updateFrameCoords();
			if(this.isPlaying)
			{
				var self = this;
				setTimeout(function(){self.updateAnimation();}, this.frameRate);
			}
		},
		
		render: function(currContext)
		{
			if(this.visible)
			{
				currContext.save();
				currContext.translate(this.x, this.y);
				currContext.rotate(this.rotation);
				currContext.globalAlpha = this.alpha;
				currContext.drawImage(this.image, 
									  this.srcX, this.srcY, this.frameWidth, this.frameHeight,   //source rect (x,y,width,height)
								      -this.halfWidth, -this.halfHeight, this.frameWidth, this.frameHeight);   //destination rect(x,y,width,height)
				currContext.restore();
			}
		}
	};
	
	var GameObjectClass = 
	{
		JUMP_POWER: 10,
		x: 0,
		y: 0,
		vx: 0,
		vy: 0,
		health: 0,
		_spriteAnimation: undefined,
		grounded: false,
		
		jump: function()
		{
			if(grounded)
			{
				vy = JUMP_POWER;
			}
		}
	};
	
	var LevelClass =
	{
		background: undefined,
		left: 0,
		right: 0,
		top: 0,
		bottom: 0,

		init: function(image, x, y, width, height)
		{
			this.background = Object.create(_spriteAnimationClass);
			this.background.init(image, width, height, 0, 1, 1000);
			this.background.x = x;
			this.background.y = y;
			
			this.left = x - this.background.halfWidth;
			this.top = y - this.background.halfHeight;
			this.right = x + this.background.halfWidth;
			this.bottom = y + this.background.halfHeight;
		}
	};
	
	var _cameraClass =
	{
		INNER_BOUNDS_RATIO: 0.25,
		x: 0,
		y: 0,
		width: 0,
		height: 0,
		
		init: function(x, y, width, height)
		{
			this.x = x;
			this.y = y;
			this.width = width;
			this.height = height;
		},
		
		rightInnerBoundary : function()
		{
			return this.x + (this.width - this.width * this.INNER_BOUNDS_RATIO);
		},
		
		leftInnerBoundary : function()
		{
			return this.x + this.width * this.INNER_BOUNDS_RATIO;
		},
		
		topInnerBoundary : function()
		{
			return this.y + this.height * this.INNER_BOUNDS_RATIO;
		},
		
		bottomInnerBoundary : function()
		{
			return this.y + (this.height - this.height * this.INNER_BOUNDS_RATIO);
		},
		
		update : function(_player)
		{
			if(_player._spriteAnimation.x + _player._spriteAnimation.halfWidth > this.rightInnerBoundary())
			{
				var diff = (_player._spriteAnimation.x + _player._spriteAnimation.halfWidth) - this.rightInnerBoundary();
			//	console.log("scrolling right");
			//	console.log(_camera.x);
				this.x += diff;
			}
			else if(_player._spriteAnimation.x - _player._spriteAnimation.halfWidth < this.leftInnerBoundary())
			{
				var diff = (_player._spriteAnimation.x - _player._spriteAnimation.halfWidth) - this.leftInnerBoundary();
				//console.log("scrolling left");
				this.x += diff;
			}
		
			if(_player._spriteAnimation.y + _player._spriteAnimation.halfHeight > this.bottomInnerBoundary())
			{
				var diff = (_player._spriteAnimation.y + _player._spriteAnimation.halfHeight) - this.bottomInnerBoundary();
				this.y += diff;
			}
			else if(_player._spriteAnimation.y - _player._spriteAnimation.halfHeight < this.topInnerBoundary())
			{
				var diff = (_player._spriteAnimation.y - _player._spriteAnimation.halfHeight) - this.topInnerBoundary();
				this.y += diff;
			}
		},
		
		clampLevel : function(level)
		{
			this.x = clamp(this.x, level.left, level.right - this.width);
			this.y = clamp(this.y, level.top, level.bottom - this.height);
		}
	
	};
	
		
	var CANVAS_WIDTH = 700;
	var CANVAS_HEIGHT = 500;

	
	var UP = 38;
	var DOWN = 40;
	var RIGHT = 39;
	var LEFT = 37;
	var SPACE = 32;
	
	var _player_SPEED = 200; // pixels per second
	
	var _assetsLoaded = 0;
	var _assetsToLoad = new Array();
	
	var spriteAtlas = new Image();
	//spriteAtlas.src = "images/ElyYWalk.png";
	spriteAtlas.src = "images/Animation2.png";
	spriteAtlas.addEventListener("load", assetLoaded, false);
	_assetsToLoad.push(spriteAtlas);
	
	var backgroundImage = new Image();
	backgroundImage.src = "images/AnimationBackground.png";
	backgroundImage.addEventListener("load", assetLoaded, false);
	_assetsToLoad.push(backgroundImage);
	

		
	var gameObjects = new Array();
	
	//Toshi
	var _player = Object.create(GameObjectClass);
	gameObjects.push(_player);
	//Eli

	
	
	//load _player sprite
	var _playerSprite = Object.create(_spriteAnimationClass);
	_player._spriteAnimation = _playerSprite;
	_player._spriteAnimation.image = spriteAtlas;
	
	
	
	var level = Object.create(LevelClass);

	//_camera
	var _camera = Object.create(_cameraClass);
	_camera.width = CANVAS_WIDTH;
	_camera.height = CANVAS_HEIGHT;
	_camera.x = 0;
	_camera.y = 0;
	
	
	
	/*Animations*/
	var _carlos = false;
	var _walkRight = false;
	var _walkLeft = false;
	var _spaceDown = false;
	
	var keysPressed = new Array();
	window.addEventListener("keydown", function(event)
	{
		if(event.keyCode == SPACE)
		{
			if(!_spaceDown)
			{
			  _spaceDown = true;
			 }
		}
		if(keysPressed.indexOf(event.keyCode) === -1)
		{
			keysPressed.push(event.keyCode);
		}		
	}, false);
	
	window.addEventListener("keyup", function(event)
	{
		if(_spaceDown)
		{
			_spaceDown = false;
		}
		var index = keysPressed.indexOf(event.keyCode);
		if(index != -1)
		{
			keysPressed.splice(index, 1);
		}
	}, false);
	/*update animations*/
	function update_playerVelocity()
	{
		_player.vx = 0;
		_player.vy = 0;

		for(var i = 0; i < keysPressed.length; ++i)
		{
			switch(keysPressed[i])
			{
			case UP:  
				_player.vy -= 1;
				_carlos = true;
				_walkRight = false;
				_walkLeft = false;
				console.log("cookie");

				break;
			case DOWN: 
				_player.vy += 1;
				break;
			case RIGHT:
				_walkRight = true;
				_walkLeft = false;
				_carlos = false;
				_player.vx += 1;
				break;
			case LEFT:
				_walkLeft = true;
				_walkRight = false;
				_carlos = false;

				_player.vx -= 1;
				break;

			}
		}
	}
		
	function gameLoop()
	{
		window.requestAnimationFrame(gameLoop, canvas);
		update();
		render();
	}
	
	function clamp(value, min, max)
	{
		return Math.max(min, Math.min(max, value));
	}
	
	var _previousTime = Date.now();
	
	var _levelWidth = 4384;
	var _levelHeight = 1800;
	
	
	
	function update()
	{
	//update anim code here
		var deltaTime = (Date.now() - _previousTime) / 1000;
		_previousTime = Date.now();
		
		/*call the animations to play*/
		
		update_playerVelocity();
		
		//this animation is playing for toshi
		_walkLeft = true;
		//_carlos = true;
		var velocityMag = Math.sqrt(_player.vx * _player.vx + _player.vy * _player.vy);
		if(velocityMag > 0)
		{
			_player.vx /= velocityMag;
			_player.vy /= velocityMag;
		}
	
		_player._spriteAnimation.x += _player.vx * deltaTime * _player_SPEED;
		_player._spriteAnimation.y += _player.vy * deltaTime * _player_SPEED;
	
		_player._spriteAnimation.x = clamp(_player._spriteAnimation.x, _player._spriteAnimation.halfWidth, _levelWidth - _player._spriteAnimation.halfWidth);
		_player._spriteAnimation.y = clamp(_player._spriteAnimation.y, _player._spriteAnimation.halfHeight,_levelHeight - _player._spriteAnimation.halfHeight);	
		
		_camera.update(_player);
		_camera.clampLevel(level);
		
		
		if(_walkRight)
		{
			//_player._spriteAnimation.init(spriteAtlas, 94, 94, 0, 4, 128);  //walk right
			_player._spriteAnimation.init(spriteAtlas, 94, 94, 0, 57, 148);  //walk right
		}
		else if(_walkLeft)
		{
		
			_player._spriteAnimation.init(spriteAtlas, 94, 94, 300, 390, 148);  //walk right
			//_player._spriteAnimation.init(spriteAtlas, 94, 94, 31, 40, 128);  //walk left
		}
		else if(_carlos)
		{
			_player._spriteAnimation.init(spriteAtlas, 94, 94, 11, 48, 128);  //carlos
			//_player2._spriteAnimation.init(spriteAtlas, 94, 94, 0, 4, 148);  //walk right
		}
	}
	
	function removeObject(objectToRemove, array) 
	{ 
		var i = array.indexOf(objectToRemove);
		if (i !== -1)
		{
			array.splice(i, 1);
		}
	}
	
	
	function render()
	{
		context.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
		
		context.save();
		context.translate(-_camera.x, -_camera.y);
		
		level.background.render(context);
		
		for(var i = 0; i < gameObjects.length; ++i)
		{
			gameObjects[i]._spriteAnimation.render(context);
		}
		context.restore();
	}

	function assetLoaded(event)
	{
		_assetsLoaded++;
		if(_assetsLoaded === _assetsToLoad.length)
		{
			gameLoaded();
		}
	}

		
	var _player_START_X = CANVAS_WIDTH / 2;
	var _player_START_Y = CANVAS_HEIGHT/2 ;

	

	

	
	function gameLoaded()
	{
	
		_walkLeft = true;
	
		//Update player start pos on screen
		//Toshi
		
		_player._spriteAnimation.init(spriteAtlas, 94, 94, 300, 390, 128); //Toshi Left idle frame
		//_player._spriteAnimation.init(spriteAtlas, 94, 94, 1, 22, 128); 
		_player._spriteAnimation.x = _player_START_X + 190;
		_player._spriteAnimation.y  = _player_START_Y - 80;
	
		
	
	
					
		//level.init(backgroundImage, 892, 240, 984, 320);
		level.init(backgroundImage, 892, 240, 984, 300);
		
		
		for(var i = 0; i < gameObjects.length; ++i)
		{
			gameObjects[i]._spriteAnimation.play(true);
		}
		gameLoop();
	}

	
});