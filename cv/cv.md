## Evgeniya Romanova
*****

 e-mail: eur2003@mail.ru

*I want to return to the direction with I studied at the university*


 Primary level of: HTML, CSS, PHP, MySQL;

Code examples
'''

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
'''

 Course: https://htmlacademy.ru

 Education:

 -  2006 year - **THE SIBERIAN STATE AUTOMOBILE AND HIGHWAY UNIVERSITY (SIBADI)**, *Engineer of Automated systems of information control and processing*
 -  2011 year - **PLEKHANOV Russian University of Economics**, *Bachelor of Economics  with finance and credit​*
 -  2020 year - **BroAcademy**, *web programming courses*

 English:
Pre-Intermediate, *in the process of studying*
