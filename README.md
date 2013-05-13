<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">

	<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">

	<title>skrollr - parallax scrolling for the masses</title>

	<link href="examples/fixed-positioning.css" rel="stylesheet" type="text/css" />
	<link href="examples/main.css" rel="stylesheet" type="text/css" />
</head>

<body>
	<div id="skrollr-body">
		<div id="bg1" data-0="background-position:0px 0px;" data-end="background-position:-500px -10000px;"></div>
		<div id="bg2" data-0="background-position:0px 0px;" data-end="background-position:-500px -8000px;"></div>
		<div id="bg3" data-0="background-position:0px 0px;" data-end="background-position:-500px -6000px;"></div>
		<div id="progress" data-0="width:0%;background:hsl(200, 100%, 50%);" data-end="width:100%;background:hsl(920, 100%, 50%);"></div>

		<div id="intro" data-0="opacity:1;top:3%;transform:rotate(0deg);transform-origin:0 0;" data-500="opacity:0;top:-10%;transform:rotate(-90deg);">
			<h1><a href="https://github.com/Prinzhorn/skrollr">skrollr</a></h1>
			<h2>parallax scrolling for the masses</h2>
			<p>let's get scrollin' ;-)</p>
			<p class="arrows">▼&nbsp;▼&nbsp;▼</p>
		</div>

		<div id="transform" data-500="transform:scale(0) rotate(0deg);" data-1000="transform:scale(1) rotate(1440deg);opacity:1;" data-1600="" data-1700="transform:scale(10) rotate(3240deg);opacity:0;">
			<h2>transform</h2>
			<p>scale, skew and rotate the sh** out of any element</p>
		</div>

		<div id="properties" data-1700="top:100%;" data-2200="top:0%;" data-3000="display:block;" data-3700="top:-100%;display:none;">
			<h2>all numeric properties</h2>
			<p>width, height, padding, font-size, z-index, blah blah blah</p>
		</div>

		<div id="easing_wrapper" data-0="display:none;" data-3900="display:block;" data-4900="background:rgba(0, 0, 0, 0);color[swing]:rgb(0,0,0);" data-5900="background:rgba(0,0,0,1);color:rgb(255,255,255);" data-10000="top:0%;" data-12000="top:-100%;">
			<div id="easing" data-3900="left:100%" data-4600="left:25%;">
				<h2>easing?</h2>
				<p>sure.</p>
				<p>let me dim the <span data-3900="" data-4900="color[swing]:rgb(0,0,0);" data-5900="color:rgb(255,255,0);">lights</span> for this one...</p>
				<p data-5900="opacity:0;font-size:100%;" data-6500="opacity:1;font-size:150%;">you can set easings for each property and define own easing functions</p>
			</div>

			<div class="drop" data-6500="left:15%;bottom:100%;" data-9500="bottom:0%;">linear</div>
			<div class="drop" data-6500="left:25%;bottom[quadratic]:100%;" data-9500="bottom:0%;">quadratic</div>
			<div class="drop" data-6500="left:35%;bottom[cubic]:100%;" data-9500="bottom:0%;">cubic</div>
			<div class="drop" data-6500="left:45%;bottom[swing]:100%;" data-9500="bottom:0%;">swing</div>
			<div class="drop" data-6500="left:55%;bottom[WTF]:100%;" data-9500="bottom:0%;">WTF</div>
			<div class="drop" data-6500="left:65%;bottom[inverted]:100%;" data-9500="bottom:0%;">inverted</div>
			<div class="drop" data-6500="left:75%;bottom[bounce]:100%;" data-9500="bottom:0%;">bounce</div>
		</div>

		<div id="download" data-10000="top[cubic]:100%;border-radius[cubic]:0em;background:rgb(0,50,100);border-width:0px;" data-12000="top:10%;border-radius:2em;background:rgb(190,230,255);border-width:10px;">
			<h2>the end</h2>
			<p>by the way, you can also animate colors (you did notice this, didn't you?)</p>
			<p><strong>Now get this thing on <a href="https://github.com/Prinzhorn/skrollr">GitHub</a> and spread the word, it's open source!</strong> <a href="https://twitter.com/share" class="twitter-share-button" data-url="http://prinzhorn.github.com/skrollr/" data-via="Prinzhorn">Tweet</a>
			<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script></p>
			<p>Check out more <a href="https://github.com/Prinzhorn/skrollr/tree/master/examples#examples">examples</a>.</p>
			<p>Handcrafted by <a href="https://twitter.com/Prinzhorn" class="twitter-follow-button" data-show-count="false">Follow @Prinzhorn</a>
			<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script></p>
		</div>
	</div>

	<script type="text/javascript">
	if(location.search === '?debug') {
		document.write('<script type="text/javascript" src="https://getfirebug.com/firebug-lite.js"><' + '/script>');
	}
	</script>

	<script type="text/javascript" src="dist/skrollr.min.js"></script>

	<script type="text/javascript">
	//http://detectmobilebrowsers.com/ + tablets
	(function(a) {
		if(/android|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(ad|hone|od)|iris|kindle|lge |maemo|meego.+mobile|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows (ce|phone)|xda|xiino|playbook|silk/i.test(a)
		||
		/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(di|rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0,4)))
		{
			//Add skrollr mobile on mobile devices.
			document.write('<script type="text/javascript" src="dist/skrollr.mobile.min.js"><\/script>');
		}
	})(navigator.userAgent||navigator.vendor||window.opera);
	</script>

	<!--[if lt IE 9]>
	<script type="text/javascript" src="dist/skrollr.ie.min.js"></script>
	<![endif]-->

	<script type="text/javascript">
	var s = skrollr.init({
		beforerender: function(data) {
			//console.log('beforerender');
		},
		render: function() {
			//console.log('render');
		},
		easing: {
			WTF: Math.random,
			inverted: function(p) {
				return 1-p;
			}
		}
	});
	</script>
</body>

</html>
