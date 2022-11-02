---
title: Student Signup
permalink: /signup/
layout: notebook
---
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
form{
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
<form action="/action_page.php" method="post">
  <img src="https://media.istockphoto.com/vectors/colorful-birds-sitting-on-beautiful-trees-isolated-on-white-vector-id1290215420?k=20&m=1290215420&s=612x612&w=0&h=8clhSXAVOIorv-5Q0C5QNIBlAQDC8Vtn54uHj3TuaQc=">
  <div class="container">
    <label for="uname"><b>Username</b></label>
    <input type="text" placeholder="Enter Github" name="uname" required>
    <label for="psw"><b>Password</b></label>
    <input type="password" placeholder="Enter Password" name="psw" required>
      <label for="psw"><b>Confirm Password</b></label>
    <input type="password" placeholder="Enter Password" name="psw" required>
    <button type="submit">Signup</button>
  </div>
</form>

</body>
</html>