# Nexis Hub — apps natives (interface)

Apps natives de Nexis Hub, une par système :

- `app_ios/` : SwiftUI, Liquid Glass d'iOS 26 et 27 (iOS 18 minimum).
- `app_android/` : Kotlin, Jetpack Compose, Material 3 (Android 8 minimum).

Ce dépôt ne contient **que l'interface**, avec des données fictives : aucun
appel réseau, aucun argent, aucun secret. Le service Nexis Hub (serveur,
paiements, bot) vit dans un dépôt privé séparé, d'où ces dossiers sont
copiés.

## Lancer

- iOS (Mac avec Xcode 26 ou plus) : `brew install xcodegen`, puis
  `cd app_ios && xcodegen generate && open NexisHub.xcodeproj`.
- Android (Android Studio) : ouvrir `app_android/`.

## Compilation automatique

`.github/workflows/apps.yml` compile et teste les deux apps à chaque envoi,
puis publie :

- `nexis-hub-android-apk` : l'APK à installer sur un téléphone Android ;
- `nexis-hub-ios-simulateur` : l'app pour le simulateur iOS (Xcode ou Appetize) ;
- `nexis-hub-ios-ipa` : une `.ipa` non signée, à signer pour un vrai iPhone ;
- des captures d'écran des deux apps.

## Licences

Code : © Nexis Hub, tous droits réservés (aucune licence de réutilisation).
Polices Inter et Unbounded : SIL Open Font License (`app_ios/NexisHub/Resources/Fonts`,
`app_android/licences`). Pictogrammes : Phosphor Icons et Tabler Icons, licence MIT.
