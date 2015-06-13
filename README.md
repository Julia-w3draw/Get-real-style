# Get-real-style
An easy way to have the computed style at hand.

For massive usage of "computed style" I use an approach, that shortens drastically the code and the execution time. I created a function called  _get_global_style() that dynamically adds to all elements an C member in which I stored the style members, in this way it could be accessed from anywhere.

function _get_global_style(){

	var all = document.getElementsByTagName("*");
	
	for(var c=0; c<all.length;c++){		
	
		all[c].C=window.getComputedStyle(all[c])
		
	}
	
}
