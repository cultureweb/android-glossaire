##### Question 1 👉 Définissez la différence entre objet, orienté objet et fonctionnel ? Comment qualifie-t-on ces concepts ? Qu’est ce qu’un POJO ?

La différence entre la programmation procédurale et la programmation orientée objet (POO) réside dans le fait que dans la programmation procédurale, les programmes sont basés sur des fonctions, et les données peuvent être facilement accessibles et modifiables, alors qu’en programmation orientée objet, chaque programme est constitué d’entités appelées objets, qui ne sont pas facilement accessibles et modifiables.
POJO est un acronyme qui signifie plain old Java object que l'on peut traduire en français par bon vieil objet Java. C’est un objet simple sans annotations ni héritage

##### Question 2 👉 Définissez la différence entre un langage interprété et un langage compilé ? Citez quelques exemples de langage.

**1. Langages interprétés et langages compilés**	 	
On peut distinguer deux grands types de langages : les langages interprétés et les langages compilés. Pour les langages supportés sur le site on a :
* langages interprétés : Java (+ JavaScool) et Python ;
* langages compilés : C, C++, Pascal et OCaml.

**2. Langages interprétés**
Dans ces langages, le code source (celui que vous écrivez) est interprété, par un logiciel qu'on appelle interpréteur. Celui-ci va utiliser le code source et les données d'entrée pour calculer les données de sortie :
 
L'interprétation du code source est un processus « pas à pas » : l'interpréteur va exécuter les lignes du code une par une, en décidant à chaque étape ce qu'il va faire ensuite.

**3.Langages compilés**
Dans ces langages, le code source (celui que vous écrivez) est tout d'abord compilé, par un logiciel qu'on appelle compilateur, en un code binaire qu'un humain ne peut pas lire mais qui est très facile à lire pour un ordinateur. C'est alors directement le système d'exploitation qui va utiliser le code binaire et les données d'entrée pour calculer les données de sortie :
 
**4.Principales différences**
On pourrait discuter très longtemps des avantages et inconvénients des différents types de langages mais les deux points qui sont les plus intéressants sont les suivants :
•	Dans un langage interprété, le même code source pourra marcher directement sur tout ordinateur. Avec un langage compilé, il faudra (en général) tout recompiler à chaque fois ce qui pose parfois des soucis.
•	Dans un langage compilé, le programme est directement exécuté sur l'ordinateur, donc il sera en général plus rapide que le même programme dans un langage interprété.
En pratique
Selon le langage que vous choisissez il y aura, ou non, cette étape de compilation. Ne soyons donc pas étonnés si, dans le prochain cours, il faut 1 ou 2 étapes selon le langage choisi.

##### Question 3 👉 Définissez les points de différence entre un langage fortement typé et faiblement voire non typé ? Citez quelques exemples de langage.
En informatique, un langage de programmation est dit fortement typé lorsqu'il garantit que les types de données employés décrivent correctement les données manipulées. Par opposition, un langage sans typage fort est dit faiblement typé. 
Il est assez difficile de donner une définition précise du typage fort. Un langage est fortement typé si :
la compilation ou l'exécution peuvent détecter des erreurs de typage. Sinon, le langage est dit faiblement typé ;
les conversions implicites de types sont formellement interdites. Si de telles conversions sont possibles, le langage est faiblement typé. Exemples répondant à ce critère : OCaml, Haskell, PureScript.
Avec cette dernière approche, on pourrait par exemple obtenir le classement suivant :
Typage	Fort	Faible
Statique	Ada, C++, Java, Pascal, ou même Visual Basic avec l'Option Explicit	Langage C : short add (int x, int y) { return x+y; }
Dynamique	Ruby, Python
JavaScript : "2" + 4 → "24"
(Dans l'exemple JavaScript, l'ambigüité provient de ce qu'un même symbole, +, est employé pour représenter aussi bien la concaténation que l'addition, selon le contexte).

##### Question 4 👉 Chercher la différence entre les deux mots clés et expliquer avec vos mots à l’enseignant.
les mot-clé val et var sont tous utilisés lors de la création de variables, la différence entre ce deux mot-clés est qu’ une variable déclarée avec le mot clé val est immuable ou constant une fois déclarer elle ne peut plus changer sa valeur initiale , tandis que une variable déclarée avec le mot-clé var est mutable sa valeur peut changer .

https://medium.com/@davidkathoh/introduction-%C3%A0-kotlin-les-variables-types-de-variable-et-le-commentaire-2106f9526389


##### Question 5 👉 Que se passe-t’il lorsque vous compilez ?
En Kotlin si on indique pas explicitement qu’une variable peut contenir une valeur null alors c’est impossible de build.
	
##### Question 6 👉 Selon vous quelle est la signature de la fonction networkCall ? Ecrivez la et faites valider par l’enseignant.
```
fun networkCall() : String ?
```

Une signature c’est déclaration sans l’implémentation comme dans une interface par exemple.


##### Question 7 👉 Comment pourriez vous faire pour exécuter du code dans le cas ou la valeur de lunwrapping 🌮 est effectivement null, pour déclencher un nouvel appel réseau par exemple ? Trouvez l’opérateur adéquat et inscrivez le code d’exemple complété dans un ficher.
```
func myNetworkResponse?.let { responseData ->
    //La fonction `let` permet de unwrap 🌮 votre variable
    saveNetworkResponseToDataBase(responseData) 
} ?:networkcall()
```


##### Question 8 👉 Quel est l’équivalent du switch en kotlin ?

In Kotlin, if is an expression, i.e. it returns a value. Therefore there is no ternary operator (condition ? then : else), because ordinary if works fine in this role.

##### Question 9 👉 Créez un tableau de string et affichez chaque valeur dans la sortie console. Faites valider par l’enseignant.
```
fun main(){
val myArray = listOf("toto", "tata", "tutu");
for(item in myArray){
    print("coucou $item, ")
}
}
```






##### Question 10 👉 Trouvez 3 exemples de classe enum qui vous permettrait de simplifier un problème ?

prints RED, GREEN, BLUE
gender MALE FEMALE
transport VOITURE VELO 

## Seconde Partie ##

##### Question 1 👉 Qu’est ce que AVD ? Que faut-il faire pour utiliser votre smartphone en tant qu’appareil de test pour votre app ?

AVD (Android Virtual Device )

##### Question 2 👉 A quoi servent les dossiers suivants :
**Layout**
Un layout définit la structure visuelle d'une interface utilisateur, telle que l'interface utilisateur d'une activité ou d'un widget d'application . Vous pouvez déclarer une mise en page de deux manières :

Déclarez les éléments d'interface utilisateur en XML . Android fournit un vocabulaire XML simple qui correspond aux classes et sous-classes View, telles que celles pour les widgets et les mises en page.
Instanciez les éléments de disposition lors de l'exécution . Votre application peut créer des objets View et ViewGroup (et manipuler leurs propriétés) par programme.

**Values**
Le dossier values est utilisé pour stocker les valeurs des ressources utilisées dans de nombreux projets Android pour inclure des fonctionnalités de couleur, de styles, de dimensions, etc. 

**Drawable**

Créez des dessins (drawables) à partir d'images de ressources
Vous pouvez ajouter des graphiques à votre application en référençant un fichier image à partir des ressources de votre projet. Les types de fichiers pris en charge sont PNG (préféré), JPG (acceptable) et GIF (déconseillé). Les icônes d'application, les logos et autres graphiques, tels que ceux utilisés dans les jeux, conviennent bien à cette technique.

Pour utiliser une ressource d'image, ajoutez votre fichier au répertoire res / drawable / de votre projet. Une fois dans votre projet, vous pouvez référencer la ressource image à partir de votre code ou de votre mise en page XML. Dans les deux cas, il est fait référence à l'utilisation d'un ID de ressource, qui est le nom de fichier sans l'extension de type de fichier. Par exemple, référez-vous à my_image.png comme my_image.

**Strings**

**colors**
**styles**
**java**
**generatedJava** ?
**Le fichier AndroidManifest.xml ?**

