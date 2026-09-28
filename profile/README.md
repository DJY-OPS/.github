<p align="center">
  <img src="https://raw.githubusercontent.com/DJY-OPS/.github/main/profile/assets/banner.svg" alt="DJY-OPS · CU_RACING · Build. Measure. Learn." width="100%">
</p>

<h1 align="center">대자연 CU_RACING 소프트웨어 아카이브</h1>

<p align="center">
  차량을 움직이는 코드부터, 주행을 읽는 데이터까지.<br>
  대자연 CU_RACING의 개발 경험을 기록하고 다음 시즌으로 이어갑니다.
</p>

<p align="center">
  <a href="https://github.com/DJY-OPS?tab=repositories">프로젝트 둘러보기</a> ·
  <a href="#development-direction">앞으로의 방향</a> ·
  <a href="https://github.com/DJY-OPS/.github/blob/main/docs/REPOSITORY_GUIDE.md">저장소 생성 가이드</a>
</p>

---

## About DJY-OPS

**DJY-OPS는 대자연 CU_RACING의 차량 소프트웨어와 팀 운영 도구를 모으는 개발 공간입니다.**

EV·BAJA 차량의 펌웨어, 텔레메트리, 주행 데이터 분석 도구와 현장 운영 소프트웨어를 함께 관리합니다. 코드와 함께 배선, 통신 정의, 실행 방법, 검증 결과를 남겨 다음 팀원이 개발을 이어갈 수 있는 아카이브를 지향합니다.

**계측 → 수집·기록 → 시각화·분석 → 차량 개선 → 다음 시즌의 자산**

## Projects

| 프로젝트 | 개발 영역 | 담고 있는 것 |
| :--- | :--- | :--- |
| [DJY_EVTLMT](https://github.com/DJY-OPS/DJY_EVTLMT) | EV 텔레메트리 | STM·ESP·BMS·GPS 수집, 실시간 피트 화면, 세션 저장과 분석 |
| [DJY_EVTQV](https://github.com/DJY-OPS/DJY_EVTQV) | EV 토크 벡터링 | 전방·후방 STM32 펌웨어, 센서 계측, 토크 배분과 통신 |
| [DJY_EVDTV](https://github.com/DJY-OPS/DJY_EVDTV) | 주행 기록 뷰어 | CSV 기반 오프라인 분석, GPS 경로, 기록을 담은 HTML 공유 |
| [DJY_EVENGM](https://github.com/DJY-OPS/DJY_EVENGM) | 에너지미터 작업 도구 | ESP32-S3 SWD 브리지, FSK Energy Meter 펌웨어 기록·복구 절차 |
| [DJY_BAJA_TLMTSYS](https://github.com/DJY-OPS/DJY_BAJA_TLMTSYS) | BAJA 텔레메트리 | Rapid Bike ECU 데이터 수신, GPS·IMU, 랩타이밍과 피트월 |
| [DJY_ChkList](https://github.com/DJY-OPS/DJY_ChkList) | 팀 운영 | 장비 체크리스트 공유, 실시간 동기화와 작업 이력 |

각 프로젝트의 현재 적용 버전과 검증 범위는 연결된 README를 기준으로 확인합니다. 에너지미터는 ESP 브리지 준비·기록까지 검증되었으며, 미터 실물의 SWD 연결과 기록은 검증 전입니다.

## How we build

- **현장에서 시작합니다.** 차량과 피트에서 필요한 기능을 만들고, 실제 운용 피드백을 다음 개선에 반영합니다.
- **원본과 근거를 남깁니다.** 측정 시각·단위·신호 출처를 기록하고, 실측값·계산값·제어 요구값을 구분합니다.
- **재현할 수 있게 정리합니다.** 코드, 빌드·실행 방법, 배선·프로토콜, 시험 조건과 결과를 함께 관리합니다.
- **상태를 명확히 기록합니다.** 개발 중인 기능, 벤치 검증, 실차 적용, 과거 자료를 구분합니다.
- **다음 팀원이 이어갑니다.** 시행착오와 변경 이유를 문서로 남기고, 시즌별 적용 버전을 추적합니다.

<a id="development-direction"></a>

## 앞으로의 방향

아래는 기존 프로젝트를 바탕으로 이어갈 개발 방향입니다. 구현 완료 여부와 일정은 각 저장소에서 관리합니다.

| 방향 | 다음으로 쌓아갈 것 |
| :--- | :--- |
| **수집과 기록의 신뢰성** | 연결 복구, 표본 시각 보존, 누락·오류 확인, 유선·무선 운용 절차 정리 |
| **데이터로 설명하는 차량** | 배터리·전력·주행·랩 데이터를 함께 분석하고, 동일 조건에서 변경 전후 비교 |
| **검증을 거치는 제어 개발** | 센서 보정, 토크 배분과 통신 변경을 시험하고 소스·설정·적용 결과를 연결 |
| **공유 가능한 분석 환경** | CSV·오프라인 뷰어 활용, 신호 이름·단위·파일 형식과 세션 정보 정리 |
| **팀의 개발 자산 축적** | 설치·복구 문서, 검증 기록, 릴리스와 인수인계 자료를 프로젝트별로 축적 |

## Repository convention

새 프로젝트 저장소는 **`DJY_프로젝트이름`** 형식으로 만듭니다.

```text
DJY_<PROJECT_NAME>

DJY_EVTLMT        EV 텔레메트리
DJY_EVTQV         EV 토크 벡터링
DJY_BAJA_TLMTSYS  BAJA 텔레메트리
```

1. **이름은 역할이 드러나게.** `DJY_` 뒤에 영문 프로젝트명 또는 뜻을 설명할 수 있는 약어를 사용합니다. 새 이름은 대문자와 `_`를 기본으로 합니다.
2. **저장소는 독립된 목적 단위로.** 함께 실행·검증하는 펌웨어와 소프트웨어는 한 저장소의 폴더로 관리하고, 독립적으로 배포·재사용하는 도구는 분리합니다.
3. **새 시즌은 버전으로 이어가기.** 같은 프로젝트의 연도별 복제보다 태그·릴리스와 적용 기록을 우선합니다. 목표나 하드웨어가 크게 달라지면 분리 이유를 남깁니다.
4. **처음부터 실행과 인수인계까지.** README에 목적, 현재 상태, 설치·실행, 구성, 검증 범위, 다음 작업을 적습니다.

기존 저장소 이름은 유지합니다. 조직 소개를 위한 `.github`는 GitHub에서 사용하는 특수 이름입니다.

**[저장소 생성 기준과 README 기본 틀 보기 →](https://github.com/DJY-OPS/.github/blob/main/docs/REPOSITORY_GUIDE.md)**

---

<p align="center">
  <b>Build. Measure. Learn.</b><br>
  한 번의 주행 경험을, 다음 개발의 출발점으로.
</p>
