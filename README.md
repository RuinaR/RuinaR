# 최원준 | Game Client Programmer

C++ / C# / Unity / DirectX 기반으로 게임 클라이언트와 미니 게임엔진·에디터 구조를 구현하고 있는 개발자 지망생입니다.

단순히 기능을 화면에 붙이는 것보다,  
그 기능이 어떤 구조 안에서 동작하고, 어떻게 저장·복원되며, 이후에 어떻게 유지보수될 수 있는지를 고민합니다.

Unity 프로젝트에서는 UI, 데이터 로드, 세이브, 스킬 시스템을 구현하며 게임 클라이언트 기능의 기본 흐름을 익혔고,  
이후 C++ 기반 엔진/에디터 프로젝트에서는 GameObject-Component 구조, SceneData 저장/로드, EditorApp/GameApp 실행 분리, DLL 기반 게임 로직 분리 구조를 직접 구현했습니다.

현재는 게임 클라이언트 개발자로서 객체 생명주기, 데이터 흐름, 런타임 구조, 에디터 툴 제작 역량을 중심으로 성장하고 있습니다.

---

## Tech Stack

### Main

![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=csharp&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![DirectX9](https://img.shields.io/badge/DirectX9-107C10?style=flat-square&logo=windows&logoColor=white)
![Win32API](https://img.shields.io/badge/Win32API-0078D6?style=flat-square&logo=windows&logoColor=white)

### Sub

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pygame](https://img.shields.io/badge/Pygame-000000?style=flat-square)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

---

## Main Projects

### [KirbyEngine](https://github.com/RuinaR/KirbyEngine)

C++17 / Win32API / DirectX9 기반 미니 게임엔진 및 에디터 프로젝트입니다.  
Unity의 GameObject-Component 구조와 에디터/런타임 실행 흐름을 참고해, C++ 환경에서 직접 엔진 구조를 구성했습니다.

**주요 구현 내용**

- GameObject-Component 기반 객체 구조
- Transform, Parent-Child 계층 구조
- EditorApp / GameApp 실행 책임 분리
- EngineFrameworkDll / EngineEditor / KirbyGameDll 구조 분리
- JSON 기반 SceneData 저장 및 로드
- ComponentFactory 기반 컴포넌트 재생성
- Object-ID 기반 참조 복원 구조
- Box2D 기반 Physics2D 및 Collision / Trigger 이벤트 전달
- ImGui 기반 Hierarchy / Inspector / ResourceBrowser / Debug Log 에디터 UI

**문제 해결 경험**

- 런타임 포인터를 그대로 저장할 수 없는 문제를 id, type, key/path 기반 직렬화 구조로 해결
- 로드 이후 resolve pass를 통해 Object-ID를 실제 참조로 복원
- Update / Collision 순회 중 오브젝트 삭제 문제를 pending add/remove 큐와 프레임 경계 처리로 해결
- DLL 간 ImGui Context가 달라지는 문제를 Context Bridge 방식으로 정리

---

### [Unity_ClickerGame_StarLight](https://github.com/RuinaR/Unity_ClickerGame_StarLight)

Unity / C# 기반 모바일 클릭커 게임 프로젝트입니다.  
별빛 재화를 수집하고 우주선을 업그레이드하는 클릭커 게임으로, UI 구조와 데이터 저장 흐름을 중심으로 구현했습니다.

**주요 구현 내용**

- JSON 기반 게임 데이터 로드
- MainUI / SubUI / ElementUI 계층 구조
- PlayerPrefs 기반 자동 저장
- 스킬 쿨타임 저장 및 유지
- 업그레이드 시스템
- 큰 숫자 단위 변환 시스템
- 다이얼로그 출력 시스템

---

### [GUI_CodeBuilder](https://github.com/RuinaR/GUI_CodeBuilder)

Flutter / Dart 기반 GUI 코드 생성 툴 프로젝트입니다.  
드래그 앤 드롭으로 GUI를 구성하고, 공통 IR을 통해 여러 플랫폼 코드로 Export하는 구조를 구현했습니다.

**주요 구현 내용**

- 위젯 트리 기반 에디터 상태 관리
- page_ir.json 기반 저장 및 로드
- 공통 IR 구조 설계
- 플랫폼별 Exporter 분리
- Flutter / Flet / PyQt / HTML-CSS Export 구조
- Property Panel 기반 속성 편집
- GitHub Pages 기반 Web Demo 배포

---

### [cover_based_duel_ai](https://github.com/RuinaR/cover_based_duel_ai)

Python / Pygame 기반 엄폐 전투 AI 강화학습 실험 프로젝트입니다.  
1:1 전투 상황에서 AI가 관측값을 바탕으로 행동을 선택하고, 보상을 통해 정책을 갱신하는 구조를 실험했습니다.

**주요 구현 내용**

- 전투 환경과 시각화 모드 분리
- Observation / Action / Reward 구조 설계
- Q-Table 기반 행동 선택
- train / visual 실행 모드 분리
- 체크포인트 저장 및 로드

---

## Team Project / Collaboration

### [HiYoung Safety AI Monitor](https://github.com/kimwook123/hiyoung_team_github)

미래내일 일경험 프로젝트형으로 진행한 산업 안전 AI 모니터링 팀 프로젝트입니다.  
영상 파일 또는 스트림에서 작업자 안전모 미착용, 위험구역 침입 등의 이벤트를 탐지하고,  
Python AI Worker / FastAPI Server / Flutter GUI로 분리된 구조에서 이벤트와 클립을 조회할 수 있도록 구성했습니다.

**담당 구현 내용**

- Python AI Worker 기반 이벤트 처리 프레임워크 설계
- DetectionResult / Event / EventFilter 기반 이벤트 상태 관리 구조 구현
- JSONL 이벤트 직렬화 및 FastAPI 서버 연동 구조 구현
- Flutter GUI의 API 이벤트 목록 / 상세 / 서버 상태 패널 연동
- 실행 가이드와 구조 문서 정리

**Commit Evidence**

- [프레임워크 완성 및 문서 보강](https://github.com/kimwook123/hiyoung_team_github/commit/7d7da14d2b8adb4832e88a9e31cd71bca3f77749)
- [서버 이벤트/클립 저장소 구조 정리](https://github.com/kimwook123/hiyoung_team_github/commit/5ffdb2d59ed481fce095651fdaf474424322efda)
- [API 이벤트 상세 패널 추가](https://github.com/kimwook123/hiyoung_team_github/commit/19c54175656553a21fa26ea89ceaf350034e1745)
- [API 서버 Health 패널 추가](https://github.com/kimwook123/hiyoung_team_github/commit/be997540eb932859999765f1a8a6866871aed112)

---

## Portfolio Focus

제가 프로젝트에서 중점적으로 다룬 부분은 다음과 같습니다.

- 게임 오브젝트 구조 설계
- 컴포넌트 기반 기능 확장
- 씬 데이터 저장 / 로드
- 런타임 객체와 저장 데이터의 분리
- 객체 생명주기 관리
- 에디터 툴 제작
- 문제 해결 과정 문서화

기능 구현에만 머무르지 않고,  
게임 플레이를 안정적으로 지탱하는 구조와 데이터 흐름을 고민하는 게임 클라이언트 개발자로 성장하고 싶습니다.

---

## Contact

- GitHub: [github.com/RuinaR](https://github.com/RuinaR)
- Email: ruina00120@gmail.com
