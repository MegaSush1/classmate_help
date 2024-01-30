# Echo : Le printf un peu spécial

Le echo inrtroduit directement son argument en tant qu'**HTML** pure.

C'est à dire que si nous feson ceci:
```
echo "<ul>
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
<li>Item 4</li>
</ul>";
```
Le résulta html visuelle sera :

* Item 1
* Item 2
* Item 3
* Item 4

### Combiner variable et text constant

Pour combiner des variables et du textes, nous pouvons le faire de 2 façons différentes :
```
$variable1 = "Saint-Roch"
$variable2 = 5

echo "Je suis à l'école " + $variable1 + " et je suis en " + $variable2 + " éme année";
```
Résulta attendu HTML: ```Je suis à l'école Saint-Roch et je suis en 5 éme année```
Maintenant, il peut des fois se produire une erreur puisque nous concaténons plusieur donnée de différents type en un.
Pour éviter cette erreur potentielle, il est plus préférable d'utiliser la version PHP de la concaténation.
Pour se faire, il suffit de juste remplacer les + par des points.
```
$variable1 = "Saint-Roch"
$variable2 = 5

echo "Je suis à l'école " . $variable1 . " et je suis en " . $variable2 . " éme année";
```

Conclusion : Il est préférable d'utiliser le point plutôt que l'opérateur plus est recommandé.
