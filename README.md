<!DOCTYPE html>
<html>
<head>
	
	<meta name="viewport" content="width=device-width,height=device-height,initial-scale=1.0" />
	<title>Sign Up</title>
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
	<style type="text/css">
		body{
			background: rgb(152,119,220);
			background: linear-gradient(0deg, rgba(152,119,220,1) 11%, rgba(164,136,221,1) 37%, rgba(189,172,221,1) 67%, rgba(201,189,221,1) 86%);
			font-family: sans-serif;
			background-repeat: no-repeat;
			background-attachment: fixed;
			background-size: cover;
		}
		.main{
			
			margin: 0 auto;
			width: 600px;
			height: 600px;
			background-color: white;
			margin-top: 25px;
			border-radius: 20px;
		}
		.main .heading{
			width: 600px;
			height: 70px;
			
			
			border-top-left-radius: 20px;
			border-top-right-radius: 20px;
			background: #6464c1;

		}
		.main .heading h2{
			/*text-align: center;*/
			position: fixed;
			margin-top: 20px;
			margin-left: 250px;
			color: white;


		}
		.main .body{
			width: 500px;
			height: 450px;
			margin: 0 auto;
			
			margin-top: 60px;
		}
		.main .body form{
			text-align: center;
			margin-top: 25px;
		}
		.input-1{
			width: 190px;
			height: 25px;
			margin: 0px 10px;
			border-radius: 5px;
			border-width: 1px;
		}
		.input-2{
			width: 410px;
			height: 25px;
			margin-top: 15px;
			border-radius: 5px;
			border-width: 1px;
			
		}
		.dob label{
			float: left;
			margin-top: 25px;
			margin-left: 43px;
		}
		.input-3{
			float: left;
			margin: 15px 20px;
			width: 180px;
			height: 25px;
			border-radius: 5px;
			border-width: 1px;
		}
		.input-4{
			width: 300px;
			margin-top: 65px;
			margin-left: 42px;
			
			padding: 0px;
			text-align: left;
		}
		.input-4 #female{
			margin-left: 25px;
		}
		.input-5{
			float: right;
			margin-right: 50px;
			margin-top: 20px;
			width: 80px;
			height: 30px;
			background-color: green;
			color: white;
			border-radius: 5px;
		}
		.text{
			
			width: 400px;
			margin-left: 45px;
			margin-top: 30px;
		}
		@media screen and (min-width: 100px) and (max-width: 199px)
		{
		    .button
		    {
		        width: 25px;
		    }
		}

		@media screen and (min-width: 200px) and (max-width: 299px)
		{
		    .button
		    {
		        width: 50px;
		    }
		}

	</style>
</head>
<body>
	<div class="main">
		<div class="heading">
			<h2>Sign Up</h2>
		</div>
		<div class="body">
			<form>
				<input class="input-1" type="text" id="firstname" placeholder="First Name">
				<input class="input-1" type="text" id="lastname" placeholder="Last Name">
				<input class="input-2" type="text" id="mobilenumber" placeholder="Mobile Number">
				<input class="input-2" type="password" id="password" placeholder="Password">
				<input class="input-2" type="password" id="re-enterpassword" placeholder="Re-enter password">
				<br>
				<div class="dob">
					<label>Date of Birth</label>
					<input class="input-3" type="date" id="dateofbirth">
				</div>
				<div class="input-4">
					
					<input type="radio" name="gender" value="male" id="male"><label for="male">Male</label>

					<input type="radio" name="gender" value="female" id="female"><label for="female">Female</label>
				</div>
				<div class="text">
					<h5>By clicking Sign Up, you agree to our Terms and that you have read our Data Policy, including our Cookie Use.</h5>
				</div>
				<button class="input-5" type="submit" id="submit">Sign Up</button>
			</form>
		</div>
	</div>
	<script type="text/javascript">
		$(document).ready(function(){
			
			$("#submit").click(function(){

				var firstname = $("#firstname").val();
				var lastname = $("#lastname").val();
				var mobilenumber = $("#mobilenumber").val();
				var password1 = $("#password").val();
				var password2 = $("#re-enterpassword").val();
				var dob = $("#dateofbirth").val();
				var gender = $("input[type='radio']:checked");
				
				if (firstname.length == 0){
					alert("Please enter user Firstname!");
				}
				else if(lastname.length == 0){
					alert("Please enter user lastname!");
				}
				else if(mobilenumber.length == 0){
					alert("Please enter user mobile number!");
				}
				else if(password1.length == 0){
					alert("Please enter a password!");
				}
				else if(password2.length==0){
					alert("Please re-enter your password!");
				}
				else if(password1!=password2){
					alert("password incorrect");
				}
				else if(dob.length==0){
					alert("Please enter your Date of Birth!");
				}
				else if(gender.val()==undefined){
					alert("please select your gender!");
				}
				else{
					alert("Sign up successfull.");
				}
			});
		})
	</script>
</body>
</html>
