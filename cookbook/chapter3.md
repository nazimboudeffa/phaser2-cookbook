# Niveau 3 : Cordon Bleu

Dans ce dernier chapitre, nous examinerons des expériences plus complexes, mais pas sur JavaScript lui même, nous allons continuer à nous concentrer sur Phaser CE.

## Comment créer une animation avec un Atlas Json Array

### Problème

Vous souhaitez animer une image-objet avec un fichier Atlas Json.

Pour cela, vous aurez besoin de texturepacker et d'un ensemble de sprites.

Prenons Raiden de l'exemple de combat mortel.

### Solution

Premièrement il faut charger le tableau atlas json array dans la fonction preload

```
  this.load.atlasJSONArray(
    'raiden',
    'raiden.png',
    'raiden.json'
  );
```

Ajouter l'animation dans la fonction create

```
  raiden = this.add.sprite(50, 100, 'raiden','01.gif');
  anim = raiden.animations.add('idle', [0,1,2,3,4,5,6,7,8,9]);
  anim.play(10, true);
```

![Mortal Combat](images/raiden.png)
