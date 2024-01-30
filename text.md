# classmate_help

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
