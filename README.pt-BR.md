# Ocultar o notch · Hide the MacBook Notch

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · **Português (BR)**

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)

**Faça o notch desaparecer.** Um app de barra de menus para macOS, minúsculo e open source, que pinta a barra superior de preto para o notch se fundir com a borda — **sem tocar no seu papel de parede**. Opcionalmente, cantos arredondados na área de trabalho.

![A barra de menus vira uma borda preta contínua e a área de trabalho ganha cantos arredondados](docs/screenshot-1.jpg)

## Por que mais um app de notch?

A maioria segue o caminho oposto: transforma o notch em uma Dynamic Island com música, timers e bandeja de arquivos. Este faz o contrário — **tira o notch da vista**, como se esconde a moldura da tela.

A diferença em relação às soluções que editam o papel de parede:

- O papel de parede continua seu — **papéis dinâmicos seguem funcionando**
- Um clique e tudo volta ao normal
- Sem permissão de gravação de tela ou acessibilidade, sem conexão de rede

## Recursos

- **Barra de menus em preto puro** — o notch se funde com a borda superior
- **Cantos da tela arredondados** — a área de conteúdo vira um retângulo arredondado, raio ajustável de 8 a 48 pt
- **Compatível com tela cheia** — sai da frente em vídeos, jogos e apresentações
- **Monitores externos intactos** — age apenas em telas com notch
- **Acompanha resolução e Spaces** — os cantos deslizam junto com a área de trabalho
- **Zero permissões, zero rede**

## Comparativo

|  | Este app | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| Ocultar o notch | ✅ | ✅ via papel de parede | ❌ o torna útil | ❌ o torna útil |
| Modifica o papel de parede | **Nunca** | Sim | – | – |
| Papéis dinâmicos | ✅ | ❌ | – | – |
| Cantos arredondados | ✅ ao vivo | ✅ embutidos no papel | ❌ | ❌ |
| Código aberto | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| Preço | Grátis | Grátis | Pago | Grátis |

## Instalação

1. Baixe `FuckBangs-1.3.3.dmg` em [Releases](../../releases/latest)
2. Arraste para **Aplicativos**
3. A primeira abertura é bloqueada pelo Gatekeeper (sem notarização). Vá em **Ajustes do Sistema → Privacidade e Segurança → "Abrir assim mesmo"**.

**Requisitos:** macOS 13 Ventura ou superior. Um MacBook com notch (MacBook Pro de 14"/16", MacBook Air a partir do M2). Em Macs sem notch o app instala, mas não faz nada.

Documentação completa, compilação a partir do código e notas de implementação: [English README](README.md).

## Licença

MIT — veja [LICENSE](LICENSE).
