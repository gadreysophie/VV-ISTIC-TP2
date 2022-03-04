# Using PMD

Pick a Java project from Github (see the [instructions](../sujet.md) for suggestions). Run PMD on its source code using any ruleset. Describe below an issue found by PMD that you think should be solved (true positive) and include below the changes you would add to the source code. Describe below an issue found by PMD that is not worth solving (false negative). Explain why you would not solve this issue.

## Answer

### PMD

J'ai utilisé PMD sur le projet Apache Common-Collection.

Pour cela, j'ai installé PMD puis j'ai cloné le projet Apache.
Ensuite j'ai utilisé lancer PMD à partir de PowerShell avec la commande suivante : 
C:\Users\gadre\pmd-bin-6.43.0\bin\pmd.bat -dir C:\Users\gadre\IdeaProjects\_Modules_VV\commons-collections -format html -R rulesets/java/quickstart.xml -language java -debug > result.html

Cela m'a permis de récupérer un fichier html reprenant toutes les recommandations/erreurs recensées par PMD. J'ai mis ce fichier result.html dans le dépôt git du TP.

#### Describe below an issue found by PMD that you think should be solved (true positive) and include below the changes you would add to the source code.

Voici le problème detécté que j'ai choisi : 

* Emplacement : C:\Users\gadre\IdeaProjects\_Modules_VV\commons-collections\src\main\java\org\apache\commons\collections4\CollectionUtils.java 
* Ligne 629	
* Problème: Use equals() to compare object references.

Voici le code associé : 
if (helper.cardinalityA.size() !=helper.cardinalityB.size()) {
            return false;
        }
        
Voici la correction demandée :
 if(!helper.cardinalityA.size().equals(helper.cardinalityB.size())
 
#### Describe below an issue found by PMD that is not worth solving (false negative). Explain why you would not solve this issue.

Voici un faux négatif : 

* Emplacement : C:\Users\gadre\IdeaProjects\_Modules_VV\commons-collections\src\main\java\org\apache\commons\collections4\ArrayStack.java	
* Ligne 155	
* Problème : Useless parentheses.

PMD informe qu'il y a des parenthèses inutiles mais celles ci permettent en fait de rendre le code plus lisible.
