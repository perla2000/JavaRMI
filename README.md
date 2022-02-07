# JavaRMI
Mise en oeuvre du service Calculator en utilisant Java RMI
## Calculator est le contrat
![calculator](https://user-images.githubusercontent.com/88480955/152702608-e7f73280-6316-4268-a6eb-2ef91ce7b45d.PNG)
## CalculatorImpl est l'implémentation du service distant
![calculatorImpl](https://user-images.githubusercontent.com/88480955/152702637-17f47f93-ec51-4452-9699-0dad4d7ea9ab.PNG)
## Execution du Programme 
### 1- Démarer notre rmiregistry en premier 
Démarer "rmiregistry" veut dire demarer le localhost sur le port 1099.
"rmiregistry" est un serveur de naming pour associe une url avec lobjet calculator 

![rmireg](https://user-images.githubusercontent.com/88480955/152702525-3893b3d4-a3eb-4e02-a5a3-303674e0aeef.PNG)

### 2- Démarer le serveur
CalculatorServeur fait un rebind d'une chaine sur rmiregistry avec l'objet CalculatorImpl qu'on a instancié
Après compilation de ce code:
![calculatorserver](https://user-images.githubusercontent.com/88480955/152702555-f6010cbc-b3d8-4da9-b87c-75fd6e1e8725.PNG)
Démarer le serveur:
![serveur](https://user-images.githubusercontent.com/88480955/152766311-dee42d50-6f3f-49a7-910f-196c240ac848.png)

### 3- Démarer le client
Le client est entrain de faire un lookup, d'obtenir dynamiquement le stub et d'invoquer les fonctions add, mult, sub etc..!
Après compilation de ce code:
![calculatorClient](https://user-images.githubusercontent.com/88480955/152702778-aa780e2e-c139-4736-a459-5bc9d9b62bf5.PNG)
Démarer le client:
![lient](https://user-images.githubusercontent.com/88480955/152766404-a618f84c-68d9-45f8-990c-d98a7d5b30ef.png)
##  Résultat:
Après avoir démarer les 3 terminaux on obtient les résultats suivants

![serverclient](https://user-images.githubusercontent.com/88480955/152702818-06ad18a9-1480-4b94-a9e8-7aa5ad60b133.PNG)
