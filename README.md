#### Question 1 👉 Définissez la différence entre objet, orienté objet et fonctionnel ? Comment qualifie-t-on ces concepts ? Qu’est ce qu’un POJO ?

La différence entre la programmation procédurale et la programmation orientée objet (POO) réside dans le fait que dans la programmation procédurale, les programmes sont basés sur des fonctions, et les données peuvent être facilement accessibles et modifiables, alors qu’en programmation orientée objet, chaque programme est constitué d’entités appelées objets, qui ne sont pas facilement accessibles et modifiables.
POJO est un acronyme qui signifie plain old Java object que l'on peut traduire en français par bon vieil objet Java. C’est un objet simple sans annotations ni héritage

#### Question 2 👉 Définissez la différence entre un langage interprété et un langage compilé ? Citez quelques exemples de langage.

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

#### Question 3 👉 Définissez les points de différence entre un langage fortement typé et faiblement voire non typé ? Citez quelques exemples de langage.
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

#### Question 4 👉 Chercher la différence entre les deux mots clés et expliquer avec vos mots à l’enseignant.
les mot-clé val et var sont tous utilisés lors de la création de variables, la différence entre ce deux mot-clés est qu’ une variable déclarée avec le mot clé val est immuable ou constant une fois déclarer elle ne peut plus changer sa valeur initiale , tandis que une variable déclarée avec le mot-clé var est mutable sa valeur peut changer .

https://medium.com/@davidkathoh/introduction-%C3%A0-kotlin-les-variables-types-de-variable-et-le-commentaire-2106f9526389


#### Question 5 👉 Que se passe-t’il lorsque vous compilez ?
En Kotlin si on indique pas explicitement qu’une variable peut contenir une valeur null alors c’est impossible de build.
	
#### Question 6 👉 Selon vous quelle est la signature de la fonction networkCall ? Ecrivez la et faites valider par l’enseignant.
```
fun networkCall() : String ?
```

Une signature c’est déclaration sans l’implémentation comme dans une interface par exemple.


#### Question 7 👉 Comment pourriez vous faire pour exécuter du code dans le cas ou la valeur de lunwrapping 🌮 est effectivement null, pour déclencher un nouvel appel réseau par exemple ? Trouvez l’opérateur adéquat et inscrivez le code d’exemple complété dans un ficher.
```
func myNetworkResponse?.let { responseData ->
    //La fonction `let` permet de unwrap 🌮 votre variable
    saveNetworkResponseToDataBase(responseData) 
} ?:networkcall()
```


#### Question 8 👉 Quel est l’équivalent du switch en kotlin ?

In Kotlin, if is an expression, i.e. it returns a value. Therefore there is no ternary operator (condition ? then : else), because ordinary if works fine in this role.

#### Question 9 👉 Créez un tableau de string et affichez chaque valeur dans la sortie console. Faites valider par l’enseignant.
```
fun main(){
val myArray = listOf("toto", "tata", "tutu");
for(item in myArray){
    print("coucou $item, ")
}
}
```






#### Question 10 👉 Trouvez 3 exemples de classe enum qui vous permettrait de simplifier un problème ?

prints RED, GREEN, BLUE
gender MALE FEMALE
transport VOITURE VELO 

## Seconde Partie ##

#### Question 1 👉 Qu’est ce que AVD ? Que faut-il faire pour utiliser votre smartphone en tant qu’appareil de test pour votre app ?

AVD (Android Virtual Device )

#### Question 2 👉 A quoi servent les dossiers suivants :
**Layout**
Un layout définit la structure visuelle d'une interface utilisateur, telle que l'interface utilisateur d'une activité ou d'un widget d'application . Vous pouvez déclarer une mise en page de deux manières :

Déclarez les éléments d'interface utilisateur en XML . Android fournit un vocabulaire XML simple qui correspond aux classes et sous-classes View, telles que celles pour les widgets et les mises en page.
Instanciez les éléments de disposition lors de l'exécution . Votre application peut créer des objets View et ViewGroup (et manipuler leurs propriétés) par programme.

**Values**

Le dossier de valeurs(values) contient des fichiers XML qui contiennent des valeurs simples, telles que des chaînes, des entiers et des couleurs. Le dossier des valeurs est utilisé pour garder une trace des valeurs que vous utiliserez dans votre application. Pour créer des applications avec un cycle de maintenance plus facile, il est fortement recommandé de ne plus coder en dur les valeurs dans votre code. Au lieu de cela, placez des valeurs dans des fichiers XML à l'intérieur du dossier de valeurs. Lorsque vous créez un nouveau projet avec Android Studio,

Vous trouverez ci-dessous les fichiers XML suivants seront générés automatiquement dans le dossier res / values:

* colors.xml
* strings.xml
* styles.xml

**Drawable**

Créez des dessins (drawables) à partir d'images de ressources
Vous pouvez ajouter des graphiques à votre application en référençant un fichier image à partir des ressources de votre projet. Les types de fichiers pris en charge sont PNG (préféré), JPG (acceptable) et GIF (déconseillé). Les icônes d'application, les logos et autres graphiques, tels que ceux utilisés dans les jeux, conviennent bien à cette technique.

Pour utiliser une ressource d'image, ajoutez votre fichier au répertoire res / drawable / de votre projet. Une fois dans votre projet, vous pouvez référencer la ressource image à partir de votre code ou de votre mise en page XML. Dans les deux cas, il est fait référence à l'utilisation d'un ID de ressource, qui est le nom de fichier sans l'extension de type de fichier. Par exemple, référez-vous à my_image.png comme my_image.

**Strings**

l'un des fichiers de valeurs les plus importants et les plus utilisés est le **strings.xml** en raison de son applicabilité dans le projet Android. La fonction de base de strings.xml est de définir les chaînes dans un fichier afin qu'il soit facile d'utiliser la même chaîne à différentes positions dans le projet Android et que le projet soit moins désordonné.
Nous pouvons également définir un tableau dans ce fichier.

Ci-dessous est mentionnée l'implémentation de la ressource strings.xml:
* filter_none
* luminosité_4
```
<resources> 
    <string name="app_name">Workshop app</string> 
  
    <string name="navigation_drawer_open">Open navigation drawer</string> 
    <string name="navigation_drawer_close">Close navigation drawer</string> 
    <string name="action_settings">Settings</string> 
    <string name="hello_blank_fragment">Hello blank fragment</string> 
    <string name="date">Date:</string> 
    <string name="timings">Timings:</string> 
</resources> 
```
Android studio donne un avertissement dans les xml de mise en page si une chaîne est utilisée dans ce fichier, il est donc recommandé de stocker toutes les chaînes codées en dur dans le fichier strings.xml.

**colors**

colors.xml est un fichier XML qui est utilisé pour stocker les couleurs des ressources.
Un projet Android contient 3 couleurs essentielles à savoir: 

* couleurPrimaire
* colorPrimaryDark
* colorAccent

Ces couleurs sont également utilisées dans certaines ressources prédéfinies du studio Android. Ces couleurs devaient être opaques, sinon cela pourrait entraîner des exceptions.

**styles**

Un autre fichier important dans le dossier de valeurs est le **styles.xml** où tous les thèmes du projet Android sont définis. Le thème de base est donné par défaut avec la possibilité de personnaliser ou d'apporter également des modifications au thème personnalisé. Chaque thème a un attribut parent qui définit la base du thème. Il y a beaucoup d'options à choisir en fonction des besoins du projet Android.
Ci-dessous est mentionnée l'implémentation de la ressource styles.xml:
filter_none
luminosité_4
```
<resources> 
  
    <!-- Base application theme. --> 
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar"> 
        <!-- Customize your theme here. --> 
        <item name="colorPrimary">@color/colorPrimary</item> 
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item> 
        <item name="colorAccent">@color/colorAccent</item> 
    </style> 
  
    <style name="AppTheme.NoActionBar"> 
        <item name="windowActionBar">false</item> 
        <item name="windowNoTitle">true</item> 
    </style> 
  
    <style name="AppTheme.AppBarOverlay" parent="ThemeOverlay.AppCompat.Dark.ActionBar" /> 
  
    <style name="AppTheme.PopupOverlay" parent="ThemeOverlay.AppCompat.Light" /> 
  
</resources> 
```
Si une fonctionnalité utilisée dans le dossier des fichiers dans les valeurs ne correspond pas à la version minimale du SDK de l'utilisateur, Android Studio donne la possibilité de définir un fichier distinct avec le même nom mais pour un niveau d'API différent. Par exemple., Styles et styles (v21) [pour les niveaux d'API de 21 et plus].

**java**

 Il s'agit du dossier de votre projet où vous stockerez tous les fichiers de code source écrits en langage de programmation Java.

`MainActivity.java` est automatiquement créé dans ce dossier par Android Studio. Toutes vos classes seront disponibles ici, et Android Studio regroupera même le chemin du package afin que vous puissiez travailler avec les fichiers sans avoir à parcourir les dossiers qui composent votre package.

**generatedJava** ?


**Le fichier AndroidManifest.xml ?**

Le fichier AndroidManifest.xml est généré dans le manifest d'Android Studio lorsque vous créez un projet. Ce fichier contient les paramètres de configuration du projet tels que les autorisations, les services et les bibliothèques supplémentaires. Un fichier manifeste fournit également des informations au système d'exploitation et à Google Play Store sur votre application.

#### Question 3 👉 Pour expérimenter tout cela du bout de vos doigts, réalisez le second tutoriel (1.2) Codelabs jusqu’à l’étape 5 en utilisant le data binding, puis faites valider par l’enseignant.

#### Question 4 👉 Comment faites vous pour que le click d’un bouton sur l’interface lance une fonction de votre code ? Quel concept de la programmation objet est utilisé dans ce cas ?

Le nom du button qui fait un eventlistener et dans son implementation appelle la fonction
rollButton.setOnClickListener { rollDice() }