# Masquer l'encoche · Hide the MacBook Notch

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md) · **Français** · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)

**Faites disparaître l'encoche.** Une minuscule app de barre des menus pour macOS, open source, qui remplit la barre supérieure de noir pour que l'encoche se fonde dans le bord — **sans jamais toucher à votre fond d'écran**. En option, des coins arrondis pour le bureau.

![La barre des menus devient un bord noir continu, le bureau gagne des coins arrondis](docs/screenshot-1.jpg)

## Pourquoi une énième app d'encoche ?

La plupart font l'inverse : elles transforment l'encoche en Dynamic Island avec musique, minuteurs et tiroirs de fichiers. Celle-ci fait le contraire : **elle la retire du champ de vision**, comme on masque un bord d'écran.

La différence avec les solutions qui modifient le fond d'écran :

- Votre fond reste le vôtre — **les fonds dynamiques continuent de s'animer**
- Un clic et tout revient comme avant
- Aucune autorisation d'enregistrement d'écran ni d'accessibilité, aucune connexion réseau

## Fonctionnalités

- **Barre des menus en noir pur** — l'encoche se fond dans le bord supérieur
- **Coins d'écran arrondis** — la zone de contenu devient un seul rectangle arrondi, rayon réglable de 8 à 48 pt
- **Compatible plein écran** — s'efface pour les vidéos, jeux et présentations
- **Écrans externes préservés** — n'agit que sur les écrans dotés d'une encoche
- **Suit la résolution et les Spaces** — les coins glissent avec le bureau
- **Zéro permission, zéro réseau**

## Comparatif

|  | Cette app | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| Masquer l'encoche | ✅ | ✅ via le fond d'écran | ❌ la rend utile | ❌ la rend utile |
| Modifie le fond d'écran | **Jamais** | Oui | – | – |
| Fonds dynamiques | ✅ | ❌ | – | – |
| Coins arrondis | ✅ en direct | ✅ intégrés au fond | ❌ | ❌ |
| Open source | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| Prix | Gratuit | Gratuit | Payant | Gratuit |

## Installation

1. Téléchargez `FuckBangs-1.3.3.dmg` depuis [Releases](../../releases/latest)
2. Glissez l'app dans **Applications**
3. Le premier lancement est bloqué par Gatekeeper (app non notariée). Allez dans **Réglages Système → Confidentialité et sécurité → « Ouvrir quand même »**.

**Configuration requise :** macOS 13 Ventura ou ultérieur. Un MacBook avec encoche (MacBook Pro 14"/16", MacBook Air à partir du M2). Sur un Mac sans encoche, l'app s'installe mais ne fait rien.

Documentation complète, compilation depuis les sources et notes d'implémentation : [English README](README.md).

## Licence

MIT — voir [LICENSE](LICENSE).
