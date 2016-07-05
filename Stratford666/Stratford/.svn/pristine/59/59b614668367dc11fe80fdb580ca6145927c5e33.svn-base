 <?php
 
    $link = mysqli_connect("earz.netfirmsmysql.com","d60274290","d60274290","d60274290"); 
    if (mysqli_connect_errno()) 
    {
      echo "Failed to connect to MySQL: " . mysqli_connect_error();
    }

    //echo 'Connected successfully'; 

    $sql="INSERT INTO  registrations  (firstname, lastname, email, ACBLnum, hometown, staying)
          VALUES
          ('$_POST[firstname]','$_POST[lastname]','$_POST[email]', '$_POST[ACBLNum]', '$_POST[hometown]', $_POST[staying])";

    $result = mysqli_query($link,$sql);
    if($result)
    {
       header('Location: reg-success.html');     
    }
    else
    {
       header('Location: reg-fail.html');
    }
    mysqli_close($link);
    exit;
?> 
