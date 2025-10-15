# Testing

## 🛠️ Comment Utiliser ce dépôt

Pour cloner ce projet, ouvrez un terminal de commande avec le chemin vers l'emplacement où vous voulez placer cet atelier et utilisez la commande suivante :

```bash
git clone --branch main-fr https://github.com/ai4devop/TS-JS-TestWithAI.git
```

Ensuite, installez les dépendances nécessaires :

```bash
npm install
```

### Comment exécuter les tests :

1. Lancez les tests avec :

```bash
npm test
```

2. Assurez-vous que tous les tests passent avant de passer à la suite.

## Objectif
Le but de cet exercice est de découvrir comment utiliser les outils d'IA pour vous assister dans la pratique du test driven development.

Pour rappel le test driven development ou TDD consiste en le fait de rédiger des test unitaires avant la création même du code. La rédaction de ces tests permet de définir le comportement attendu par les fonctions. Une fois le code rédigé, les tests peuvent être lancés pour valider le comportement.

Dans cet exercice, vous retrouverez la classe utils qui a pour objectif d'offrir des fonctions utilitaires pour le traitement de dates avec ou sans heures. Vous serez amenés à rédiger des tests pour les fonctions que nous souhaitons implémenter et ensuite le code des fonctions.

### Instructions

- Clonez ce projet.
- Rendez vous dans le fichier `utils` pour prendre connaissance des squelettes de méthodes crée et dans `utils.test` pour voir les tests implémentés.
- Réalisez les différentes implémentations décrites dans la partie étapes du bas
- Lancer les tests déjà présents et ceux que vous aurez écrits

### 1. TDD - Rédaction de fonctions à partir de tests (20 minutes)
Pour la première partie de cette exercise, nous allons rédiger des fonctions pour le traitement de `Date`. Dans la classe `utils.test`, une serie de tests unitaires ont été rédigés qui dictent le comportement attendu par 3 fonctions. Il faudra maintenant s'appuyer sur Continue pour rédiger le code de ces fonctions en fonction du tests unitaire.

- **Implémentez la méthode `formatDate(LocalDate date)`** :
   - Il faudra partir du test `testFormatDate_ValidDate` déjà rédigé dans `utils.test`
   - Cette méthode doit accepter un objet `Date` et retourner un `String` au format `yyyy-mm-dd`.
   - Utilisez le chat IA pour générer le code

- **Implémentez la méthode `parseDate(String date)`** :
   - Il faudra partir du test `testParseDate_ValidDate` déjà rédigé dans `utils.test`
   - Cette méthode doit accepter un `String` au format `yyyy-mm-dd` et retourner un objet `Date`.
   - Réalisez cette exercice en utilisant la sélection de code du chat IA

- **Implémentez la méthode `formatDateWithPattern(LocalDate date, String pattern)`** :
   - Il faudra partir du test `testFormatDate_WithPattern` déjà rédigé dans `utils.test`
   - Cette méthode doit accepter un objet `Date` et un `String` qui contiendra le pattern de la date attendu, ex : 'yyyy-mm-dd' et retourner un `String` avec la date au format attendu.
   - Réalisez cet exercice en utilisant le copiant votre test dans le chat IA


### 2. Rédaction de tests unitaires par description (15 minutes)
Sur cette deuxième partie de l'exercice, nous allons nous attaquer aux object `Date`. Cette fois-ci, il faudra rédiger des tests qui dicteront le comportement des fonctions, puis enchainer avec la rédaction de la fonction.
- **Pour la fonction `formatDateTime(Date dateTime)`** :
   - Rédigez un premier test `testFormatDateTime_ValidDateTime` qui vérifiera que pour une `Date` donnée, la fonction `formatDateTime` retourne bien une chaine de caractère, _ex : "2024-08-31T08:46:00"_
   - Ce test échouera bien sûr car la fonction appelée n'est pas encore implémentée
   - Une fois le test rédigé, vous pouvez vous attaquer à la rédaction de fonction `formatDateTime(Date dateTime)`
   - Assurez vous que le test que vous avez rédigé passe maintenant
   - Utilisez l'auto-complétion par commentaire pour réaliser cette exercice

- **Pour la fonction `parseDateTime(String dateTimeString)`** :
   - Rédigez un premier test `testParseDateTime_ValidDateTime` qui vérifiera que pour une `String` donnée, au format yyyy-MM-ddThh:mm:ss,  la fonction `parseDateTime` retourne bien un objet `Date`, _ex : "2024-08-31T08:46:00"_
   - Rédigez un deuxième test `testParseDateTime_InvalidDateTime` qui vérifiera que pour une `String` pas au format yyyy-MM-ddThh:mm:ss, la fonction `formatDateTime` échoue bien avec une exception `DateTimeParseException`, _ex : "invalid-date"_
   - Ces tests échoueront bien sûr car la fonction appelée n'est pas encore implémentée
   - Une fois les tests rédigés, vous pouvez vous attaquer à la rédaction de fonction `parseDateTime(String dateTimeString)`
   - Assurez vous que les tests que vous avez rédigés passent maintenant
   - Utiliser le inline code pour réaliser cet exercice (ctrl + l)

### 3. Rédaction de tests unitaires par code (10 minutes)
Sur cette dernière parties de l'exercice, nous allons nous attaquer au bloc Testing, qui va vous permettre d'écrire des tests unitaire en fonction d'un code donné
- **Pour la fonction `formatDateTime(Date dateTime, String pattern)`** :
   - Rédigez des tests unitaire dans `testFormatDateTime_WithPattern` qui vérifiera que pour une `Date` donnée et un pattern choisi, la fonction `formatDateTime` retourne bien une chaine de caractère au format donnée, _ex : avec dd/MM/yyyy HH:mm:ss on a "31/08/2024 08:46:00"_
   - Le code vous est fourni, à vous de générer les tests grâce à l'aide de l'IA
   - Réalisez cette exercice en utilisant les raccourcis Copilot (click droit > copilot)
   

### Critères de validation :

- Les fonctions pour le traitement des `Date` sont rédigés et les tests déjà écrits passent tous.
- Les tests et fonctions pour le traitement des `DateTime` sont rédigés et les tests écrits passent tous.
