$(document).ready(function ()
	{
		$('#submit').click(function ()
			{
				var fname = $('#fname').val();
				if(fname.length==0)
				{
					alert('Name field cannot be empty');
					$('#fname').focus();
					return false;

				}

				var email = $('#email').val();
				var email_regex = /^[\w\-\.\+]+\@[a-zA-Z0-9\.\-]+\.[a-zA-z0-9]{2,4}$/;
				if (!email.match(email_regex) || email.length == 0)
				{
					alert("Please enter a valid email address"); // This Segment Displays The Validation Rule For Email
					$("#email").focus();
					return false;
				}

				var number = $("#number").val();
				var number_regex = /^[0-9]+$/;

				if (!number.match(number_regex) || number.length == 0)
				{
					alert("Please enter a valid phone number "); // This Segment Displays The Validation Rule For Phone number
					$("#number").focus();
					return false;
				}

				if($('input[type=checkbox]:checked').length == 0)
				{
					alert ( "ERROR! Please select at least one checkbox" );
    				return false;
				}

				if($('input[type=radio]:checked').length==0)				
				{
					alert('Please accept terms and conditions');
					return false;
				}
			}
		)
	}
	
)

