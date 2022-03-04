# Code of your exercise

Voici le code que j'ai utilisé pour les tests sur le nombre de ifStatement :

public class useOfXpath{

public void test(){
   int a = 0;
   int b = 0;
   int c = 0;

   if (a>b){
        if (a>c){
            if (b>c){
                return c;
           }
       }
    }
    if (b>c){
        if (b>c){
            if (b>c){
                if (b>c){
                    return b;
                }
            }
        }
    }
    if (c>a){
        if (c>b){
            return c;
        }  
    }
}
}
