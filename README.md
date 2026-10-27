<div align="center">


<a href="mailto:minjaon@naver.com"><img src="https://img.shields.io/badge/Email-minjaon@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Seoul,_Korea-555555?style=flat-square"/>

</div>

---

### 📌 Featured Projects

#### 🐧 [Linux Device Driver on Jetson Orin Nano](https://github.com/minjaon/Linux_Device_Driver) `2026.10 · 4인`
> 같은 제어 로직을 **유저 공간(libgpiod/sysfs)** 과 **커널 캐릭터 디바이스 드라이버**로 각각 구현해 비교한 임베디드 리눅스 프로젝트

- **담당:** 8-Bar LED 커널 드라이버 `led_bar_driver.ko`
- 40핀 헤더에 흩어진 GPIO 8개를 하나의 `/dev/led_bar` 장치로 묶어 추상화
- `ioctl` 레벨 모드(0~8단계) / 8비트 RAW 비트마스크 모드, `echo`·`cat`으로 쓰는 `write`/`read` 인터페이스
- 모터 방향 전환 시 30ms 전체 점멸로 상태 피드백

`C` `Linux Kernel 5.15-tegra` `Character Device` `ioctl` `GPIO`

#### ♻️ [Smart Recycling Edge AI](https://github.com/minjaon/smart-recycling-edge-ai) `2026.09 · 4인`
> Jetson이 재질을 판별하면 STM32가 투입구를 여는 AI 분리수거 키오스크

- **담당:** STM32F411 MCU 펌웨어 전체 (HAL 없이 레지스터 직접 제어)
- 스타트업 코드·링커 스크립트·Makefile부터 구성, PLL 96MHz 클럭 / SysTick / USART 인터럽트 직접 설정
- TIM3 3채널 PWM 서보 **순차 인터록** — 하단 2축 도착 확인 후 상단 개방, 120°/s 소프트웨어 램프
- 부팅 시 서보 동시 구동 돌입전류로 인한 전압 강하 → 순차 정렬로 해결
- 초음파 4채널 적재율 측정 + 3단계 필터(블랭킹 → 중앙값 기반 이상치 제거 → 변화량 임계 갱신)
- Jetson ↔ STM32 UART 명령 프로토콜 (`$DOOR_OPEN`, `$BIN` …)

`C` `STM32F411` `Bare-metal` `CMSIS` `PWM` `UART` `arm-none-eabi-gcc`

#### 🚦 [Smart Gate & Traffic Light Control](https://github.com/minjaon/GUI-Cortex-M4-) `2026.08 · 4인`
> STM32 펌웨어 + PyQt5 관제 GUI + 로컬 LLM 자연어 제어

- 펌웨어(`main.cpp`)와 GUI(`main.py`) 대규모 개편
- LLM은 허용된 UART 명령으로 **변환만**, 최종 판단은 STM32 FSM — 조건이 안 맞으면 펌웨어가 명령을 거부
- 거리 연속 감지 시에만 EMERGENCY 전환해 튐 값에 의한 오동작 방지
- QThread로 시리얼 수신·LLM 호출을 UI 스레드와 분리
- 초음파 ECHO 5V → 분압 회로, 서보 구동 시 보드 리셋 → 외부 전원 분리로 해결

`C++` `STM32 HAL` `PyQt5` `UART` `Ollama`

#### 🎬 [AgeApt](https://github.com/minjaon/AgeApt) `2024.09 ~ 2025 · 4인`
> AI가 사용자 연령을 분석해 화면을 바꾸는 영화관 키오스크

- **담당:** 백엔드 · 배포 (팀 내 커밋 2위)
- 영화 조회 · 좌석 예매 · 잔여 좌석 관리 API
- TMDB(영화 데이터) · 카카오페이(결제) · CoolSMS(예매 문자) 연동
- MySQL 연동, Docker로 AWS EC2 배포

`Java` `Spring Boot` `JPA` `MySQL` `Docker` `AWS EC2`

#### 📚 [AI_2026](https://github.com/minjaon/AI_2026) — 교육 과정 실습 아카이브
ATmega128A · ARM Cortex-M4(레지스터/CMSIS: GPIO, UART, Timer, EXTI, I2C, SPI, ADC, DMA) · Qt/PyQt · YOLO(ONNX/TensorRT) 추론 실습

---

### 🛠 Tech Stack

**Embedded & Systems**<br/>
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/> <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/Linux_Kernel-FCC624?style=flat-square&logo=linux&logoColor=black"/> <img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white"/> <img src="https://img.shields.io/badge/ARM_Cortex--M4-0091BD?style=flat-square&logo=arm&logoColor=white"/> <img src="https://img.shields.io/badge/Jetson_Orin_Nano-76B900?style=flat-square&logo=nvidia&logoColor=white"/> <img src="https://img.shields.io/badge/Qt-41CD52?style=flat-square&logo=qt&logoColor=white"/>

**Application & Backend**<br/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/PyQt5-41CD52?style=flat-square&logo=qt&logoColor=white"/> <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>

**Tools & Infra**<br/>
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/Make-427819?style=flat-square&logo=gnu&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white"/> <img src="https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white"/>
