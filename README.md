<p align="center">
  <strong>한국어</strong> | <a href="README_en.md">English</a>
</p>

# Qurious Batch

**몬스터 헌터 라이즈: 선브레이크의 방어구 괴이 강화를 10회 진행하고, 결과를 한 화면에서 비교해 하나를 선택하는 PC 모드입니다.**

제작 NPC에서 평소처럼 방어구와 괴이 강화 방식을 선택하면 일괄 연성 화면이 열립니다. 재료를 납부하고 생성된 후보 10개를 비교한 뒤, 원하는 결과를 적용하거나 현재 상태를 유지할 수 있습니다.

## 주요 기능

- 일반·안정형·스킬 특화형·슬롯 특화형 방어구 괴이 강화 지원
- 10개 후보를 5×2 카드로 비교하고 선택한 후보의 상세 정보 확인
- 현재 상태와 후보의 방어력·내성·장식주 슬롯·장비 스킬 비교
- 슬롯의 실제 레벨과 스킬의 유지·추가·감소 구분 표시
- 장비 스킬 설명 및 레벨별 효과 확인
- 현재 착용 중인 전신 스킬 조회
- 재료 수동 선택·자동 선택 및 초과 포인트 반환 안내
- 키보드·마우스·컨트롤러 조작 지원
- 한국어·영어 UI 및 Nintendo·Xbox·PlayStation 버튼 표기
- 해상도 자동 배율과 80~120% 추가 배율 설정
- 마을에서 사용할 수 있는 활성화 전환 단축키와 화면 알림

## 설치

### 준비 사항

- Windows용 Steam판 **Monster Hunter Rise: Sunbreak**
- 게임에서 방어구 괴이 강화가 해금된 상태
- [REFramework](https://www.nexusmods.com/monsterhunterrise/mods/26?tab=files)

	설치하려면 zip 파일에서 dinput8.dll을 추출하여 ‘몬스터 헌터 라이즈’ 게임 설치 폴더에 넣기만 하면 됩니다.
	
	Insert 키를 누르면 메뉴를 열 수 있습니다.

### 모드 파일 배치

게임을 종료한 상태에서 다음 항목을 게임 설치 폴더에 복사합니다.

```text
MonsterHunterRise/
└─ reframework/
   ├─ autorun/
   │  ├─ QuriousBatch.lua
   │  └─ QuriousBatch/
   │     └─ *.lua
   └─ fonts/
      └─ QuriousBatch.ttf
```

### 활성화 전환

| 입력 장치 | 단축키 |
|---|---|
| Nintendo 표기 | **ZR + L스틱 누름** |
| Xbox 표기 | **RT + L스틱 누름** |
| PlayStation 표기 | **R2 + L3** |
| 키보드 | **\~ 키 + PageDown** |

단축키는 마을에서만 동작하고, 퀘스트·훈련장·로딩 중이나 일괄 연성 처리 중에는 전환하지 않습니다. 
활성화 여부는 화면 알림으로 표시됩니다. 
REFramework 설정창의 체크박스로도 전환할 수 있습니다.

## 로그와 문제 보고

아래 경로는 모두 **게임 설치 폴더 기준**입니다.

| 파일 | 내용 |
|---|---|
| `reframework/data/QuriousBatch.log` | 모드 실행, 비용, 후보 선택 및 오류 기록 |
| `re2_framework_log.txt` | REFramework 실행 로그와 Lua·네이티브 오류 기록 |
| `reframework_crash.dmp` | REFramework가 생성한 크래시 덤프. 생성되지 않을 수도 있습니다. |
| `reframework/data/QuriousBatch_settings.json` | 언어·패드 표기·배율 설정 |

크래시 직후에는 게임을 다시 실행하기 전에 로그를 복사해두세요. 덤프가 존재해도 이전 충돌의 파일일 수 있으므로 수정 시간을 확인해주세요.

문제를 보고할 때 다음 내용을 함께 남겨주시면 도움이 됩니다.

- 모드 버전, 게임 버전, REFramework 버전
- 선택한 방어구와 괴이 강화 방식
- 문제가 발생하기 직전의 조작과 사용한 입력 장치
- 오류 화면 캡처
- 위 로그 파일과, 해당 시각에 생성된 덤프
