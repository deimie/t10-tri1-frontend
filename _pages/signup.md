---
title: Student Signup
permalink: /signup/
layout: notebook
---
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">


<style>
body{
  background-color:#85d6a7;
}    
.form{
  background-color: #fff;
  border: 4px solid #b0ed8a
}  
input[type=text], input[type=password] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  border: 1px solid #ccc;
  box-sizing: border-box;
  b
}
button {
  background-color: #03989E;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  width: 100%;
}
button:hover {
  opacity: 0.8;
}
img.avatar {
  border-radius: 50%;
}
.container {
  padding: 16px;
}
span.psw {
  float: right;
  padding-top: 16px;
}
/* Change styles for span and cancel button on extra small screens */
@media screen and (max-width: 300px) {
  span.psw {
     display: block;
     float: none;
  }
}
</style>
</head>
<body>

<div class="form">
  <img src="https://media.istockphoto.com/vectors/colorful-birds-sitting-on-beautiful-trees-isolated-on-white-vector-id1290215420?k=20&m=1290215420&s=612x612&w=0&h=8clhSXAVOIorv-5Q0C5QNIBlAQDC8Vtn54uHj3TuaQc=">

  <div class="container">
    <label for="uname"><b>Username</b></label>
      <input id="uname" type="text" placeholder="Enter Github" name="uname">
    <label for="psw"><b>Password</b></label>
      <input id="psw1" type="password" placeholder="Enter Password" name="psw">
    <label for="psw"><b>Confirm Password</b></label>
      <input id="psw2" type="password" placeholder="Re-Enter Password" name="psw">
    <p id="error" style="color: red;"></p>
    <button onclick="pswSubmit()">Sign Up</button>
  </div>
</div>

</body>
</html>

 <script>
  localStorage.clear();
  localStorage.setItem("loggedIn", false);

  function pswSubmit(){
    if (document.getElementById("psw1").value == '' || document.getElementById("psw2").value == '' || document.getElementById("uname").value == '') {
        document.getElementById("error").innerHTML = "One or more fields left emtpy.";
    }
    else {
      if (document.getElementById("psw1").value == document.getElementById  ("psw2").value){
      localStorage.setItem("loggedIn", true);
      localStorage.setItem("ghUsername", document.getElementById("uname").value)

      window.location.replace("https://deimie.github.io/t10-tri1-frontend/");
      }
     else {
      document.getElementById("error").innerHTML = "Passwords do not match.";
     }
    }

    
  }
</script>