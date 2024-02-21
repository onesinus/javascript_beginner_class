### HTML Codes

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>jQuery Learn</title>
</head>
<body>
	<div id="banner-message">This is banner message</div>
	<button class="continue" id="btnShow"></button>
	<!-- <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script> -->
	<script type="text/javascript" src="https://code.jquery.com/jquery-4.0.0-beta.js"></script>
	<script type="text/javascript" src="main.js"></script>
</body>
</html>
```

```javascript
$(document).ready(function() {
	$("button.continue").html("Next Step...")

	const hiddenBox = $("#banner-message")
	hiddenBox.hide()
	$("#btnShow").on("click", function(event) {
		hiddenBox.show()
		$.ajax({url: "https://www.w3.org/TR/2003/REC-PNG-20031110/iso_8859-1.txt", success: function(result){
	    	hiddenBox.html(result);
	    }});
	})
})
```
