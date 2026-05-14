# Hackintosh-OpenCore-EliteBook840-G5
Hackintosh du HP EliteBook 840 G5

<img src="/screenshot.png"/>

## 💻 Configuration

| Specifications | Details                                                  |
| ------------------- | ------------------------------------------- |
| Version OpenCore     | 1.0.7      					|
| CPU | Intel i5-8250U (Kaby Lake R)               |
| iGPU          | Intel UHD 620            |
| Wi-Fi          | Intel AC-8265            |
| Audio          | Conexant CX8200 (ALCID=3)            |

## 🍎 Comment fonctionne un hackintosh ?

Pour comprendre le fonctionnement d'un hackintosh et plus précisément du dossier "EFI", je vous invite à regarder [ma vidéo](https://youtu.be/Gaffvrc63jk) traitant du sujet.

## 📂 Spécifications Mac

| Specifications | Details                                                  |
| ------------------- | ------------------------------------------- |
| Version max     | Sonoma 14      					|
| SMBIOS | MacBookAir8,1               |
| SIP          | Enabled `00000000`            |

Sequoia a abandonné la prise en charge du Wi-Fi Intel. Sonoma est la dernière version pleinement fonctionnelle et le modèle du Mac choisi ne proposera pas la mise à jour.

## ✅ Ce qui fonctionne

- CPU / Accélération graphique
- Gestion de la luminosité
- Ethernet
- Wi-Fi ([AirportItlwm](https://github.com/openintelwireless/itlwm/releases) est a rajouter selon la version de macOS)
- Audio (haut-parleurs et sortie casque)
- Ports USB et SD (le mappage a été fait)
- Microphone
- Trackpad et clavier

## ❌ Ce qui ne fonctionne pas

- Bluetooth
- Webcam

## ⚠️ Activation iServices

Pour activer les services Apple, il est nécessaire de faire les manipulations suivantes :
- Définir le `SecureBootModel` sur "Default" dans `Misc -> Security`. Il est désactivé par défaut pour éviter des problèmes lors de l'installation.
- Insérer l'adresse MAC de votre carte Ethernet dans `PlateformInfo -> Generic -> ROM`.
