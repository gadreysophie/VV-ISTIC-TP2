# No getter!

With the help of JavaParser implement a program that obtains the private fields of public classes that have no public getter in a Java project. 

A field has a public getter if, in the same class, there is a public method that simply returns the value of the field and whose name is `get<name-of-the-field>`.

For example, in the following class:

```Java

class Person {
    private int age;
    private String name;
    
    public String getName() { return name; }

    public boolean isAdult() {
        return age > 17;
    }
}
```

`name` has a public getter, while `age` doesn't.

The program should take as input the path to the source code of the project. It should produce a report in the format of your choice (TXT, CSV, Markdown, HTML, etc.) that lists for each detected field: its name, the name of the declaring class and the package of the declaring class.

Include in this repository the code of your application. Remove all unnecessary files like compiled binaries. See the [instructions](../sujet.md) for suggestions on the projects to use.

*Disclaimer* In a real project not all fields need to be accessed with a public getter.

## Answer

Afin de mettre en place JavaParser, j'ai téléchargé les fichiers qui se trouvent dans le répertoire code et dans le repertoire javaparser-starter.

J'ai ensuite utilisé le maven du projet avec maven install -> mvn install

J'ai également repris le code exemple proposé dans la question afin de le soumettre à javaparser.

Une fois le build sucess du maven du projet javaparser, j'ai pu soumettre mon code d'exemple à javaparser via l'utilisation d'une commande sous powershell.

Voici la commande utilisée : 
 java -jar .\target\javaparser-starter-1.0-jar-with-dependencies.jar .\src\main\java\testCode\
 
Cette commande permet de lancer l'exécution du javaparser sur les fichiers se trouvant sur le dossier testCode. Ici le fichier est exampleCode que j'ai ajouté dans le dossier code de javaparser dans le dépît git.
 
La réponse à cette commande est celle ci :
testCode.exampleCode
  public String getName()
  public String getFirstname()
  public boolean isAdult()
  
 On peut voir toutes les méthodes qui sont déclarées dans le fichier et donc ensuite vérifier s'il manque des getters ou des setters.
 
 Ici il manque les getters/setters suivants : 
 
* public void setName()
* public void setFirstname
* public int getAge()
* public void setAge()
* public String getAdresse()
* public void setAdresse()
