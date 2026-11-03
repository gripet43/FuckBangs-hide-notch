# 노치 없애기 · Hide the MacBook Notch

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · **한국어** · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)

**노치를 사라지게.** MacBook 메뉴 막대를 한 줄의 검정으로 채워 노치를 검은 테두리에 녹여버리는 가벼운 macOS 메뉴 막대 앱입니다. **배경 화면은 건드리지 않습니다.** 원하면 화면 네 모서리를 둥글게 만들 수도 있습니다.

![메뉴 막대가 하나의 검은 띠가 되고, 아래 데스크탑은 모서리가 둥글어진다](docs/screenshot-1.jpg)

## 왜 또 하나의 노치 앱인가

대부분의 노치 앱은 반대 방향입니다. 노치를 '다이내믹 아일랜드'로 만들어 음악과 타이머를 넣죠. 이 앱은 정반대입니다. **노치를 시야에서 지웁니다.**

배경 화면을 고치는 방식과 다른 점:

- 배경 화면 그대로, **동적 배경 화면도 계속 움직입니다**
- 클릭 한 번이면 원래대로
- 화면 기록·손쉬운 사용 권한 불필요, 네트워크 통신 없음

## 기능

- **메뉴 막대를 순수 검정으로** — 노치가 위쪽 테두리에 녹아들어 눈에 띄지 않습니다
- **화면 모서리 둥글게** — 콘텐츠 영역 전체를 하나의 둥근 사각형으로. 반지름 8–48pt 조절
- **전체 화면 대응** — 영상·게임·발표 중에는 자동으로 물러나고 돌아오면 복귀
- **외부 모니터는 그대로** — 노치가 있는 화면에만 적용, 외부 모니터는 직각 유지
- **해상도 대응**, **Space 전환 시 함께 슬라이드**
- **권한 없음 · 통신 없음**

## 비교

|  | 이 앱 | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| 노치 숨기기 | ✅ | ✅ 배경 화면 수정 | ❌ 활용하는 방향 | ❌ 활용하는 방향 |
| 배경 화면 변경 | **없음** | 있음 | – | – |
| 동적 배경 화면 | ✅ | ❌ | – | – |
| 화면 모서리 둥글게 | ✅ 실시간 | ✅ 배경 화면에 포함 | ❌ | ❌ |
| 오픈 소스 | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| 가격 | 무료 | 무료 | 유료 | 무료 |

## 설치

1. [Releases](../../releases/latest)에서 `FuckBangs-1.3.3.dmg` 다운로드
2. **응용 프로그램** 폴더로 드래그
3. 첫 실행은 Gatekeeper에 막힙니다(공증 없음). **시스템 설정 → 개인정보 보호 및 보안 → "그래도 열기"** 로 허용하세요.

**요구 사항:** macOS 13 Ventura 이상. 노치가 있는 MacBook(14/16인치 MacBook Pro, M2 이후 MacBook Air). 노치가 없는 Mac에서는 설치되지만 아무 효과도 없습니다.

자세한 기능, 소스 빌드, 구현 메모는 [English README](README.md)를 참고하세요.

## 라이선스

MIT — [LICENSE](LICENSE).
