# Connection PHP -> SQL

## Connexion à la database
```
<?php
$servername = ""; // Nom ou adresse du serveur sql

$username = ""; // Utilisateur utilisé

$password = ""; // Mot de passe du serveur

$dbname = ""; // Nom de la base de donné utilisé

$conn = new mysqli($servername,$username,$password,$dbname); // Établissement de la connexion à la base

if($conn->connect_error){ // vérification si la connexion avec la database est bien établie

  die("conn failed: ".$conn->connect_error); // Si connexion non réussi, alors couper celle-ci

}
  
$demande = [insert sql select command]; // commande de select sql

$result = $conn->query ($demande); // enregistrer les informations obtenus pour utilisation par la suite
?>
```
## Parcourir les données
```
<?php

if($result->num_rows>0){ // Vérifier si la liste des résultat n'est pas vide

  while($row=$result->fetch_assoc()){ // Parcourir les informations rangé par rangé

    echo $row; // Affichage des informations dans le html
// Argument : Si par exemple vous voulez récupérer l'information qui est dans la colonne appelé "description" dans la database, alors il s'écrira : $row["description"].
// Cette variable n'est quand lecture seule (aucune modification direct sur celle-ci n'est possible)
  }
}

?>
```
