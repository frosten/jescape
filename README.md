jescape
=======

jEsacpe jquery, javascript esc key event handling

<div id="header">
	This extension captures all the keydown events faster and less time writing code, you'll profit.<br />

	<h3> Methods </h3>
	<code class="language-javascript">
		.escape(callback function);
		.removeEscape();
	</code>
	
<table cellspacing="0" cellpadding="0" border="0" class="properties" style="margin-left:40px;width: auto;">
	<tbody><tr>
		<th scope="col">Arguments</th>
		<th scope="col">Type</th>
		<th scope="col">Description</th>
	</tr>	
	<tr>
		<td>callback</td>
		<td>function</td>
		<td> After press esc button than execute callback function</td>
	</tr>
</tbody></table>


<h3>How it works</h3>
	
 <code>
$(document).ready(function() { 
	$('#header').escape(function() { 
		$('#title').css('background-color', 'red');
		$('#header').removeEscape();
	});
});
</code>
 

<br />
<br />
Try this for press ESC button.

<h3> Setup </h3>
<div style="background-color: #efefef;width:600px">
&lt;script src="http://code.jquery.com/jquery-1.6.1.min.js"></script><br/>
&lt;script type="text/javascript" src="jescape.js"></script>
</div>
<br />
Use $().escape(function(){ /*TODO: Add your code*/ }); on elements when DOM is ready
<br /><br />
<div style="background-color: #efefef;width:600px">
&lt;script><br />
$(function(){<br />
&nbsp;&nbsp;$('a.anything').escape(function() { alert('TEST'); });<br />
});<br />
&lt;/script><br />
</div>
<h3> Changelog </h3>
<b>v.0.2</b><br/>
Reverse executing<br/>
Remove ESC functions<br/>
<b>v.0.1</b> <br/>
Adding array all ESC handler functions<br/>
Executing<br/>
</div>

<script type="text/javascript">
	
	var sample_jQuery_object = $('<div />');
	sample_jQuery_object.escape(function() {  
		location.href = 'http://ben.ferit.im';
	});
	
	/*Never execute, because removeEscape for this element */
	$('#development').escape(function() {
		location.href = 'http://ben.ferit.im';
	});
	
	$('body').escape(function() {
		alert('Ok, try press then back to home.');
	});

	$('#header').escape(function() { 
		$('#title').css('background-color', 'red');
	});
	
	$('#development').removeEscape();
	
	jKeyEvent.debug();
	
	
	/*You can't need this code*/
	$.SyntaxHighlighter.init({
				'wrapLines':false,
				'lineNumbers':false
	});
	</script>
</body>
</html>
