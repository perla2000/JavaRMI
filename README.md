# JavaRMI
Mise en oeuvre du service Calculator en utilisant Java RMI
## Calculator est le contrat
![calculator](https://user-images.githubusercontent.com/88480955/152702608-e7f73280-6316-4268-a6eb-2ef91ce7b45d.PNG)
## CalculatorImpl est l'implémentation du service distant
![calculatorImpl](https://user-images.githubusercontent.com/88480955/152702637-17f47f93-ec51-4452-9699-0dad4d7ea9ab.PNG)
## Execution du Programme 
### 1-  Demarer notre rmiregistry en premier 
Demarer rmiregistry veut dire demarer le localhost sur le port 1099
rmiregistry est un serveur de naming pour associe une url avec lobjet calculator 

![rmireg](https://user-images.githubusercontent.com/88480955/152702525-3893b3d4-a3eb-4e02-a5a3-303674e0aeef.PNG)

### 2-Demarer le serveur
CalculatorServeur fait un rebind d'une chaine sur rmiregistry avec l'objet CalculatorImpl qu'on a instancié

![calculatorserver](https://user-images.githubusercontent.com/88480955/152702555-f6010cbc-b3d8-4da9-b87c-75fd6e1e8725.PNG)

### 3- Demarer le client
Le client est entrain de faire un lookup, d'obtenir dynamiquement le stub et d'invoquer les fonctions add, mult, sub etc..![serverclient](https://user-images.githubusercontent.com/88480955/152702540-ecbedcdd-a4e9-4bda-8dec-fc2764744178.PNG)
