# CCN Code : Consigne 1
## Step 1 @unplugged
### Faire du bruit
Faites jouer une fréquence à votre micro::bit.

```blocks
basic.forever(function () {
    music.ringTone(365)
})
```

## Step 2 @unplugged
### Faire d'autres bruits
Essayer de changer le nombre de hertz pour faire un son plus grave, ou plus aigu.

```blocks
basic.forever(function () {
    music.ringTone(12000)
})

basic.forever(function () {
    music.ringTone(100)
})
```

## Step 3
### Faire d'autres bruits
Quand est-ce que le son est grave ? Quand est-ce qu'il est aigu ?
Quel est le minimum ? Quel est le maximum ?

## Step 4 @unplugged
### Faire plus de bruit
Ajoute la brique de volume.

```blocks
basic.forever(function () {
    music.setVolume(127)
})
```

## Step 5
### Faire plus de bruit
Change la valeur pour baisser ou monter la puissance du son.
Quel est le minimum ? Quel est le maximum ?

## Step 6 @unplugged
### Ca bouge !!!!
Nous allons maintenant utiliser l'accélérométre.
https://microbit.org/get-started/user-guide/features-in-depth/#accelerometer

En appuyant sur les boutons, tu peux voir la valeur de l'accélérométre.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(input.acceleration(Dimension.X))
})

input.onButtonPressed(Button.B, function () {
    basic.showNumber(input.acceleration(Dimension.Y))
})
```

## Step 7
### Ca bouge !!!!
Penche la carte et essaie de trouver le maximum et le minimum pour les 2 axes.

## Step 8 @unplugged
### Ensemble, on est plus forts
On va maintenant mettre ensemble l'accélérométre et le son du microbit.

Pour cela, il faut utiliser une brique mathématique qui permet de transformer les valeurs de l'accélérométre.
Qu'est ce que cette brique change ?

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.map(input.acceleration(Dimension.X), -1023, 1023, 20, 10000))
})
input.onButtonPressed(Button.B, function () {
    basic.showNumber(Math.map(input.acceleration(Dimension.Y), -1023, 1023, 0, 255))
})
```

## Step 9
### Ensemble, on est plus forts @unplugged
Maintenant que l'on connait les minimum, les maximums de tout le monde.
Peut-on piloter le son avec le geste ? Et comment ?
