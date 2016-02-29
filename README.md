# Signature Pad Demo

It is a very basic demo app to shows how to draw signatures


## How to run demo

1. Clone the the repo ```git clone git@github.com:EligibleAPI/SignaturePadExample.git```

2. Open ```require-drawn-signature.html``` with any browser

## Usage

1. Download Signature Pad

	Get the signature pad assets from our signature pad demo application

2. Import Assets

	Drop these files into your assets folder:

	    jquery.signaturepad.css
	    jquery.signaturepad.js
	    json2.min.js
	    flashcanvas.js
	    pen.cur

3. Include Javascript files

	The following code should appear in your html file header:
	
	HTML

		<link href="jquery.signaturepad.css" rel="stylesheet">
		<!--[if lt IE 9]><script src="../assets/flashcanvas.js"></script><![endif]-->
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script>
		<script src="jquery.signaturepad.js"></script>
		<script src="json2.min.js"></script>
		<script>
		  $(document).ready(function() {
		    $('.sigPad').signaturePad({drawOnly:true});
		    $('#submit').click(function () {
		      if($('input.output').val()){
		        alert($('input.output').val());
		      }
		      else{
		        alert('Please sign the document')
		      }
		    })
		  });
		</script>
		
4. Add a form

	This block of code should be added to your html body:

	HTML
	
		<form method="post" action="" class="sigPad">
		  <ul class="sigNav">
		    <li class="clearButton"><a href="#clear">Clear</a></li>
		  </ul>
		  <div class="sig sigWrapper">
		    <div class="typed"></div>
		    <canvas class="pad" width="198" height="55"></canvas>
		    <input type="hidden" name="output" class="output">
		  </div>
		  <button type="submit" id="submit">Submit.</button>
		</form>

## How to use it with Eligible - Enrollments

Please refer to complete documentation on Signature Pad here https://docs.eligible.com/docs/signatures#capturing-electronic-signatures

## More Customizations

This demo example is extracted from https://github.com/thomasjbradley/signature-pad

Please refer to https://github.com/thomasjbradley/signature-pad to check more examples and list of options available
