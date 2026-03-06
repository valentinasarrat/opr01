<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Primer ejemplo</title>
    <style>
        .parent { display: grid; grid-template-columns: repeat(3, 1fr); }
		circle {fill:pink}
		circle.tipo0{fill:red}
		circle.tipo1{fill:green}
    </style>
</head>
<body>
	<h1>holi</h1>
    <div class="parent">
        <div><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><g id="primera"></g></svg></div>
        <div><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><g id="segunda"></g></svg></div>
		<div><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><g id="tercera"></g></svg></div>
    </div>
    <script>
        const data = [20, 50, 10];
        ["primera", "segunda", "tercera"].forEach((id, i) => {
            document.querySelector(`#${id}`).innerHTML = `<circle cx="50" cy="50" r="${data[i]}" class="tipo${i}"/>`;
        });
    </script>
</body>
</html>
