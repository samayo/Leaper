
![Y U CODE LIKE THIS](http://i.imm.io/1hvBM.jpeg)

##NoodlePiece


##### vat ze hel iz zis ? 

If you are too noob, or too lazy to write those blocks PDO statements for each and simple
PDO-based CRUD applications on the fly as you code, then NoodlePiece is your noodle and your best friend. 

Let's take this as example

      
      try{
      	
          $stmt = $conn->prepare('SELECT * FROM users WHERE id = ?');
          $stmt->execute(array($_POST['id']));
       } catch(PDOException $e){
         	 echo $e->getMessage();
       }
       
       if($stmt->rowCount()){
         	
         	$row = $stmt->fetchAll(PDO::FETCH_ASSOC); 
         	return $row; 
         	
       }else{
         	echo 'Query failed';
       }


Well, in NoodlePiece, all you have to do to get the same result is... 

      $select = $NoodlePiece->doLazy->('SELECT * FROM users')->where('id = ?', $_POST['id']); 

that is it. And now, `$result` holds the required data, for your to display. 






