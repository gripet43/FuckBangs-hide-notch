# Ocultar el notch · Hide the MacBook Notch

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · **Español** · [Français](README.fr.md) · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)

**Haz que el notch desaparezca.** Una app de barra de menús para macOS, minúscula y de código abierto, que pinta la barra superior de negro para que el notch se funda con el borde superior, **sin tocar tu fondo de pantalla**. Opcionalmente redondea las esquinas del escritorio.

![La barra de menús se vuelve un borde negro continuo y el escritorio gana esquinas redondeadas](docs/screenshot-1.jpg)

## ¿Por qué otra app para el notch?

Casi todas van en la dirección contraria: convierten el notch en una Dynamic Island con música, temporizadores y bandejas de archivos. Esta hace lo opuesto: **lo quita de la vista**, como se disimula el marco de una pantalla.

La diferencia frente a las soluciones que editan el fondo:

- Tu fondo sigue siendo tuyo — **los fondos dinámicos siguen funcionando**
- Un clic y todo vuelve a como estaba
- Sin permisos de grabación de pantalla ni de accesibilidad, sin conexión de red

## Funciones

- **Barra de menús en negro puro** — el notch se funde con el borde superior
- **Esquinas redondeadas** — el área de contenido se convierte en un rectángulo redondeado, radio ajustable de 8 a 48 pt
- **Compatible con pantalla completa** — se aparta sola en vídeos, juegos y presentaciones
- **Monitores externos intactos** — solo actúa en pantallas con notch
- **Se adapta a la resolución y a los Spaces** — las esquinas se deslizan junto al escritorio
- **Cero permisos, cero red**

## Comparativa

|  | Esta app | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| Ocultar el notch | ✅ | ✅ editando el fondo | ❌ lo hace útil | ❌ lo hace útil |
| Modifica el fondo | **Nunca** | Sí | – | – |
| Fondos dinámicos | ✅ | ❌ | – | – |
| Esquinas redondeadas | ✅ en vivo | ✅ dentro del fondo | ❌ | ❌ |
| Código abierto | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| Precio | Gratis | Gratis | De pago | Gratis |

## Instalación

1. Descarga `FuckBangs-1.3.3.dmg` desde [Releases](../../releases/latest)
2. Arrástrala a **Aplicaciones**
3. El primer inicio lo bloquea Gatekeeper (sin notarización). Ve a **Ajustes del Sistema → Privacidad y seguridad → «Abrir igualmente»**.

**Requisitos:** macOS 13 Ventura o superior. Un MacBook con notch (MacBook Pro de 14"/16", MacBook Air desde M2). En equipos sin notch se instala, pero no hace nada.

Documentación completa, compilación desde el código y notas de implementación: [English README](README.md).

## Licencia

MIT — consulta [LICENSE](LICENSE).
