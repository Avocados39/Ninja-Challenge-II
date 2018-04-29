# Ninja-Challenge-II
Make Ninjaman take steps in all directions
<!DOCTYPE html>
<html>
<title>NinjaMan</title>
<body>
	<div id='background' style= 'width: 1860px; height: 900px; background-image: url("img/white_bg.jpg")'>
		<div id='character' style='position: absolute; top: 450px; left: 930px; background-image: url("img/down1.png"); width:59px; height: 86px;'></div>
	</div>
	<script type="text/javascript">
		var leftValue = 930, topValue = 450, direction = 'down', step = 1;

		document.onkeydown = function(e){
			console.log(e);
			if(step == 1){
				step = 2;
			}
			else if(step == 2){
				step = 1;
			}
		function update(){
			document.getElementById("character").style.left = leftValue + "px";
			document.getElementById("character").style.top = topValue + "px";
			document.getElementById("character").style.backgroundImage = "url('img/"+direction+step+".png')";
			}

			if(e.keyCode == 37 && leftValue > 0){ //LEFT
				leftValue = leftValue - 10;
				direction = 'left';
			}
			else if(e.keyCode == 39 && leftValue < 1860){ //Right
				leftValue = leftValue + 10;
				direction = 'right';
			}
			else if(e.keyCode == 38 && topValue > 0){ //UP
				topValue = topValue - 10;
				direction = 'top';
			}
			else if(e.keyCode == 40 && topValue < 900){ //DOWN
				topValue = topValue + 10;
				direction = 'down';
			}
			update();
		}
		
	</script>

	
</body>
</html>
