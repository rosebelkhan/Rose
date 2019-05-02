<?php 

//Difference between echo and print


	/*1. echo contains multiple parameter (ex: "Rose", "is", "Nice")
	  2. print doesn't contain multiple parameter.
	  3. echo is more faster than print.	  
	
	*/
?>



<?php
//string
	echo "I am Rosebel Khan";
		echo "<br/>";
	echo "This is the main Theme for you but you don't know that.";
echo "<br>";


//variable
$fonts="I want to be a well programmer.";
echo $fonts;
echo "<br>";


// string method
echo str_replace("programmer", "java", $fonts);
echo "<br>";
echo strrev($fonts);
echo "<br>";
echo strpos($fonts, "ram");
echo "<br>";



$a= 1;
$b= 2;
$c = $a*$b;
echo $c;
echo "<br>";
echo "Total value for the mango is: ".$c;
echo "<br>";
$x=array("amjad","pakhia","nose");
var_dump($x);

echo "<br>";
echo "<br>";
echo "<br>";

//costants
 
define("VALUE","I am a rosebel Ohp
!",true);

function rosebel(){
		return value;
	}


	echo rosebel();

echo "<br/>";
echo "<br/>";

//operators

$x = 100;
$y = "200";

var_dump($x != $y);


echo "<br/>";
echo "<br/>";
//increments operators

$z = 5;
echo $z++;
echo "<br/>";
echo $z;
echo "<br/>";
echo $z;

echo "<br/>"; echo "<br/>";

//logical operators


$a = 40;
$b = 20;

if( $a == 40 xor $b == 20 ){
	echo "Mahady Hassan";
} else {
	echo "Rosebel khan";
}

//concatanation operators

echo "<br/>"; echo "<br/>";

$d = "Khan ";
$f = "Bahadur";
$g = $d.$f;
echo $g;
echo "<br/>";
echo "<br/>";

//array operators

$v = array(
	"a" => "dhaka",
	"b" => "sylhet"
);

$c = array(
	"c" => "comilla",
	"d" => "rajshahi"
);

var_dump($v != $c);

//switch statement

echo "<br/>";
echo "<br/>";

$my = "js";

switch($my){
	
	case "php":
	echo "I love php";
	break;
	
	case "raw":
	echo "I love raw";
	break;
	
	case "js":
	echo "I love js";
	break;
	
	
	default:
	echo "i love programming";
}


echo "<br/>";
echo "<br/>";

//while loop

$l = "0";

while($l <= 5){
	echo "The no. is : $l <br/>";
	$l++;
}

//do while loop

echo "<br/>";
echo "<br/>";

$o = 1;
do{
	echo "The number is : $o <br/>";
	$o++;
}while($o <= 3);



//for loop

echo "<br/>";
echo "<br/>";

for($i = 1; $i <= 10; $i++){
	echo "the number is : $i <br/>";
}


echo "<br/>";
echo "<br/>";

//for each loop

$colors = array("blue", "green", "sky");

foreach($colors as $color){
	echo "$color <br/>";
}


echo "<br/>";
echo "<br/>";


//function
/*
function school($name = "My school"){
	echo "$name is a good school ! which invented by ! <br/>";
}

school("jatrabari high school");

school("Ml high school");
school ();
school("Rosebel khan high school");


function sum($q,$w){
	$i = $q+$w;
	return $i;
}
echo "5+10 = ".sum(5,10);

*/
//variable scope

echo "<br/>";
echo "<br/>";

$m = 20;

function test1(){
	global $m;
	$a = 5;
	echo $a;
	
echo "<br/>";
echo "This is the main no of the world: ".$m;
echo "<br/>";
}

function test2(){
	global $m;
	$b = 15;
	echo $b;
	
echo "<br/>";
echo "This is the main no. of the world :".$m;
}

test1();
test2();


//SUPER $GLOBALS / $_SERVERS / $_REQUEST / $_POST / $_GET / $_FILE / $_ENV / $_COOKIE / $_SESSION

echo "<br/>";
echo "<br/>";

//SUPER $GLOBALS

$x = 4;
$y = 16;
function sum(){
	$GLOBALS['z'] = $GLOBALS['x'] + $GLOBALS['y'];
}

sum();
echo $z;

//SUPER $_SERVERS



echo $_SERVER['HTTP_USER_AGENT'];

echo "<br/>";
echo "<br/>";


//form validation

echo "Today is :".date("Y/m/d");
echo "<br/>";
echo "<br/>";
echo "Today is :".date("l");
echo "<br/>";
echo "<br/>";
echo "Today is :".date("h:i:na");
echo "<br/>";
echo "<br/>";

echo date_default_timezone_get('Asia/Dhaka');

echo "<br/>";
echo "<br/>";
echo "<br/>";
echo "<br/>";




















































/*
//SUPER $_REQUEST

echo "<br/>";
echo "<br/>";

echo "<br/>";
echo "<br/>";
echo "<br/>";
echo "<br/>";


if($_SERVER["REQUEST_METHOD"] == "POST"){
	$name = $_REQUEST['username'];
	
	if(empty($name)){
		echo "<span style='color:red'>username is empty !</span>";
	}else {
		echo "<span style='color:green'>You have submitted :".$name."</span>";
	}
}

echo "<br/>";
echo "<br/>";

*/





?>










<form action="<?php echo $_SERVER['PHP_SELF']?>" method="post">
Username : <input type="text" name="username"/>
<input type="submit" value="submit"/>
</form>


<a href="text.php?msg=Good&text=Bye">Sent Data</a>
</br>
</br>
</br>



<form method="post" action="<?php echo htmlspecialchars($_SERVER['PHP_SELF']); ?>">


<table>

	<p style="color:red"> * required field</p>


	<tr>
		<td>Name : </td>
		<td><input type="text" name="name" placeholder="Your name" required /> <span style="color:red"> *</span></td>
	</tr>



	<tr>
		<td>E-mail : </td>
		<td><input type="text" name="email" placeholder="Your email" required /> <span style="color:red"> *</span></td>
	</tr>



	<tr>
		<td>Website : </td>
		<td><input type="text" name="website" placeholder="Your website" required /> <span style="color:red"> *</span></td>
	</tr>


	<tr>
		<td>Comment : </td>
		<td><textarea name="comment" rows="5" cols="40" placeholder="Your comment"></textarea></td>
	</tr>


	
	<tr>
		<td>Gender : </td>
		<td><input type="radio" name="gender" value="Female"/>Female 
			<input type="radio" name="gender" value="male"/>Male 
		</td>
	</tr>
	
	
	
	<tr>
		<td></td>
		<td><input type="submit" name="submit" value="Submit"/>
		</td>
	</tr>
	
	
	


</table>
</form>




<?php

$name = $email = $website = $comment = $gender = "";
$errname = $erremail = $errwebsite = $errcomment = $errgender = "";

if($_SERVER["REQUEST_METHOD"] == "POST"){
	
	$name 		= validate($_POST["name"]);
	$email	 	= validate($_POST["email"]);
	$website 	= validate($_POST["website"]);
	$comment 	= validate($_POST["comment"]);
	$gender 	= validate($_POST["gender"]);
	
	
	echo "name :".$name."<br/>";
	echo "email :".$email."<br/>";
	echo "website :".$website."<br/>";
	echo "comment :".$comment."<br/>";
	echo "gender :".$gender."<br/>";
	
}
function validate($data){
	$data = trim($data);
	$data = stripcslashes($data);
	$data = htmlspecialchars($data);
	
	return $data;
}

?>



