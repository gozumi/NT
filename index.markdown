---
layout: default
title: 
class: nt-presents
---
<style type="text/css">
	#fallback-cover {
		z-index: -9999;
		position: fixed;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		background: url(/work/imitation-34-59/assets/imitation-34-59-2.jpg) center center no-repeat;
		background-size: 100%;
		display: none;
	}
</style>


<iframe id="showcase-frame" class="showcase-frame" src="http://player.vimeo.com/video/70820493?title=0&amp;byline=0&amp;portrait=0&amp;color=939b9e&amp;autoplay=1&amp;loop=1&amp;api=1" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

<div id="showcase-cover" class="showcase-cover">
	<div class="NT"></div>
</div>

<script type="text/javascript">

require([
	'dojo/dom',
	'dojo/has',
	'dojo/dom-class',
	'dojo/dom-style',
	'dojo/_base/fx',
	'dojo/domReady!'
], function(dom, has, domClass, domStyle, fx){

	if (has('touch')) {
		domStyle.set(dom.byId('showcase-frame'), 'display', 'none');
		domStyle.set(dom.byId('fallback-cover'), 'display', 'block');
	}

	var cover = dom.byId('showcase-cover');

	fx.fadeOut({
		node: cover,
		duration: 5000,
		delay: 3000,
		onEnd: function() {
			domStyle.set(dom.byId('bottom-bar'), 'opacity', '1');
		}
	}).play();

});

</script>

<div id="fallback-cover"></div>
<noscript>
	<style type="text/css">
		#showcase-cover,
		#showcase-frame {
			display: none;
		}

		#bottom-bar {
			opacity: 1;
		}

		#fallback-cover {
			display: block;
		}
	</style>
</noscript>