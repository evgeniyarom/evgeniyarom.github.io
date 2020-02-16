#1.  Evgeniya Romanova
######2. e-mail:eur2003@mail.ru
######3. I want to return to the direction with I studied at the university

######4. Primary level of: HTML, CSS, PHP, MySQL;



######5. Code examples
'<addr>'
index.php
<?php
	header ("Content-Type: text/html; charset=utf-8");
	mysql_connect('localhost','root','');
	mysql_select_db('home');
	if($_GET['page']=='add_news'){
		include ('templates/add_news.tpl');
			if (isset ($_POST['add'])){
				$title = mysql_real_escape_string($_POST['title']);
				$autor = mysql_real_escape_string($_POST['autor']);
				mysql_query("INSERT INTO news(id, title, autor) VALUES(NULL, '$title', '$autor')");
			}
		
	}
	if($_GET['page']=='news'){
		$list=array();
		$res=mysql_query ("SELECT * FROM news");
		while($row=mysql_fetch_assoc($res)) {
			$list[]=$row;
			
		}
		include ('templates/view_news.tpl');
	}	
	if($_GET['page']=='add_fruits'){
		include ('templates/add_fruits.tpl');
			if (isset ($_POST['add'])){
				$name = mysql_real_escape_string($_POST['name']);
				$price = mysql_real_escape_string($_POST['price']);
				mysql_query("INSERT INTO fruits(id, name, price) VALUES(NULL, '$name', '$price')");
			}
		
	}
	if($_GET['page']=='view_fruits'){
		$list=array();
		$res=mysql_query ("SELECT * FROM fruits");
		while($row=mysql_fetch_assoc($res)) {
			$list[]=$row;
			
		}
		include ('templates/view_fruits.tpl');
	}	
?>
######6. Course: https://htmlacademy.ru

######7. Education:
*Item 1 2006 year - **THE SIBERIAN STATE AUTOMOBILE AND HIGHWAY UNIVERSITY (SIBADI)**, *Engineer of Automated systems of information control and processing*
*Item 2 2011 year - **PLEKHANOV Russian University of Economics**, *Bachelor of Economics  with finance and credit​*
*Item 3 2020 year - **BroAcademy**, *web programming courses*

######8. English
*Item 1 Pre-Intermediate, *in the process of studying*


