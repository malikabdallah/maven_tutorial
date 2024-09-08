# maven_tutorial


Maven permet
-La construction du livrable final
-Gestion des bibliothèque logicielles de dépendances
-Permet de publier un site et générer des rapport de qualité
-Permet la publication des versions
-Sa modularité basé sur la notion de plugin facilite l'ajout de fonctionnalités lors du cycle de vie

il y a deux notions fondamentales
-POM ecrit en xml , est l'unique descripteur du projet et seul garant
de l'identification comme project Apache maven
-Convention over configuration 

Permettre :
-Un seul point d'entrée pour la configuration
-Une structure de dossier standartisé
-Ne plus stocker les librairies de dependances


Maven est developpé en java et necessite une JDK
Rappel:
JRE => les bibliotheques logicielles , JVM 
JDK => JRE + JAVAC + DEBUG


POM(PROJECT OBJECT MODEL):
est le descripteur d un project maven  , il expose un model 

les elements obligatoire dans un pom
sont ->model version la version du model utilise
->group id , identifie le project dans un espace de nommage
-> artifact id valeur principale , le nom de l archive( minuscule et -)
-> version en cours du project

pom.xml garanti la cohérence et validité des infos contenu dans tous ces fichier suivant
un XSD .

Un XSD est un fichier au format XML chargé de definir le contrat d un document xml
comme pour le java tous les POM heritent d un pom commun le supper pom 

Configuré apache maven
qu est ce qu un referentiel:
il s agit d un emplacement sur un systeme de fichier , qui contient les bibliotheques logiciel
(jar) selon une arbo basé sur le groupid artifactid et indexe grace au fichier xml
metadata
il y a 2 type de ref
-local => emplacement sur le system local ou sont stocké les bibliotheques necessaire a maven
et project en cours de dev
->distant = distant par rapport au serveur a partir duquel les bibliotheques sont telechargé
alimente le ref local

settings xml
le principal fichier de configuration maven est le settings.xml
il est tres important dans la mise en place d un env autour de maven , 
il y en a 2
le premier dans maven_home/conf => global
le deuxieme dans /.m2/settings xml => specific utilisateur


info de base du settings xml
-> localRepository 
-> interactive mode =>si les reponses par defaut doivent etre automatiquement selectionne
-> offline => si maven doit fonctionné en mode deconnecté en utilisant uniquement son ref local
(attention peut pas demaré la premiere fois en offline il doit accedé au repo distant pour download )



