---
layout: default
title: NT Presents
class: nt-presents
---

<iframe class="showcase-frame" src="http://player.vimeo.com/video/70820493?title=0&amp;byline=0&amp;portrait=0&amp;color=939b9e&amp;autoplay=1&amp;loop=1&amp;api=1" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

<div id="showcase-cover" class="showcase-cover">
	<div class="NT"></div>
</div>
<div id="logo"></div>


<script type="text/javascript">

require([
	'dojo/dom',
	'dojo/dom-class',
	'dojo/dom-style',
	'dojo/_base/fx',
	'dojo/domReady!'
], function(dom, domClass, domStyle, fx){

	var cover = dom.byId('showcase-cover');

	fx.fadeOut({
		node: cover,
		duration: 5000,
		delay: 3000,
		onEnd: function() {
			domClass.add(dom.byId('logo'), 'logo');
			domStyle.set(dom.byId('navigation-wrapper'), 'opacity', '1');
			domStyle.set(cover, 'display', 'none');
		}
	}).play();

});

</script>