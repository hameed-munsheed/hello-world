<!DOCTYPE html>
<html>
<head>
	<title>Endless Array of Circles</title>
	<style>
		body {
			margin: 0;
			padding: 0;
			background-color: #111;
		}
		.circle {
			position: absolute;
			width: 50px;
			height: 50px;
			border-radius: 50%;
			background-color: #fff;
			animation: circle-anim 2s linear infinite;
		}
		@keyframes circle-anim {
			from {
				transform: translateX(0);
			}
			to {
				transform: translateX(calc(100vw - 50px));
			}
		}
	</style>
</head>
<body>
	<script>
		// Create endless array of circles
		for (let i = 0; i < 100; i++) {
			let circle = document.createElement('div');
			circle.classList.add('circle');
			circle.style.top = (i * 60 + 50) + 'px';
			document.body.appendChild(circle);
		}
	</script>
</body>
</html>
