<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MAEC Login Portal</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:linear-gradient(135deg,#8b0000,#d32f2f);
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
}

.login-box{
    width:400px;
    background:#fff;
    border-radius:15px;
    padding:30px;
    text-align:center;
    box-shadow:0 0 25px rgba(0,0,0,0.3);
}

.logo{
    width:120px;
    height:120px;
    object-fit:contain;
    margin-bottom:15px;
}

h2{
    color:#8b0000;
    margin-bottom:5px;
}

h3{
    color:#555;
    margin-bottom:20px;
    font-weight:normal;
}

input{
    width:100%;
    padding:12px;
    margin:10px 0;
    border:1px solid #ccc;
    border-radius:6px;
    font-size:16px;
}

button{
    width:100%;
    padding:12px;
    background:#8b0000;
    color:#fff;
    border:none;
    border-radius:6px;
    font-size:17px;
    cursor:pointer;
}

button:hover{
    background:#a00000;
}

label{
    float:left;
    margin-bottom:10px;
    font-size:14px;
}

#message{
    margin-top:15px;
    font-weight:bold;
}

.footer{
    margin-top:20px;
    color:#666;
    font-size:13px;
}
</style>

</head>
<body>

<div class="login-box">

<img src="logo.png" class="logo" alt="College Logo">

<h2>Melmaruvathur Adhiparasakthi</h2>
<h3>Engineering College</h3>

<form id="loginForm">

<input
type="text"
id="username"
placeholder="Enter Username"
required>

<input
type="password"
id="password"
placeholder="Enter Password"
required>

<label>
<input type="checkbox" onclick="showPassword()">
Show Password
</label>

<br><br>

<button type="submit">Login</button>

</form>

<p id="message"></p>

<div class="footer">
Study • Spirituality • Service
</div>

</div>

<script>

function showPassword(){

let x=document.getElementById("password");

if(x.type==="password"){
x.type="text";
}
else{
x.type="password";
}

}

document.getElementById("loginForm").addEventListener("submit",function(e){

e.preventDefault();

let username=document.getElementById("username").value;
let password=document.getElementById("password").value;

let message=document.getElementById("message");

if(username==="student" && password==="maec@123"){

message.style.color="green";
message.innerHTML="✔ Login Successful! Welcome to MAEC.";

setTimeout(function(){
window.location.href="https://www.google.com";
},1500);

}
else{

message.style.color="red";
message.innerHTML="✖ Invalid Username or Password.";

}

});

</script>

</body>
</html>
