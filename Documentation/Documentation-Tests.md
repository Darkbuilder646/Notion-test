# Documentation des Tests Unitaires

## Fonction : `add`

### Description
La fonction `add` prend deux arguments `a` et `b`, et retourne leur somme.

### Exemple de Code
```javascript
function add(a, b) {
    return a + b;
}
```

### Tests Unitaires

Pour tester cette fonction, nous allons utiliser un framework de tests unitaires comme Jest. Voici un exemple de fichier de test :

### Installation de Jest
Assurez-vous d'avoir Jest installé dans votre projet. Vous pouvez l'installer via npm :
```bash
npm install --save-dev jest
```

### Exemple de Fichier de Test
Créez un fichier nommé `add.test.js` dans votre répertoire de tests et ajoutez le code suivant :

```javascript
const add = require('./path/to/your/add/function');

test('addition de 1 et 2 pour obtenir 3', () => {
    expect(add(1, 2)).toBe(3);
});

test('addition de nombres négatifs', () => {
    expect(add(-1, -2)).toBe(-3);
});

test('addition de zéro', () => {
    expect(add(0, 0)).toBe(0);
});
```

### Exécution des Tests
Pour exécuter les tests, ajoutez le script suivant dans votre `package.json` :
```json
"scripts": {
    "test": "jest"
}
```

Ensuite, lancez les tests avec la commande :
```bash
npm test
```

### Résultats Attendus
Tous les tests devraient passer sans erreurs, confirmant que la fonction `add` fonctionne correctement pour les cas de test fournis.