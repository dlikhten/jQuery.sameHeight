# Controlling height in css is freaken' hard.

So let's say you have 3 divs that are not necessarily siblings and you need them to be of equal height. AND let's make it harder: they are not fixed height, so any one of them can be of different size at page load. Well, how do you set their height to be equal?

Using this tiny plugin it's simple.

## Usage

One thing to note: It is best if run during `window.load` event rather than in `document.ready` because only `window.load` guarantees that custom fonts and images are loaded. This is useful as the height of the elements will be fixed and not resize to the newly added content. After loading the page, any time you dynamically change the size of any of these divs, you will need to set the css `height` to `auto` and re-run this plugin 


example usage:

	$(window).load(function(){ 
		$(".we_need_to_be_equal").sameHeight();
	});