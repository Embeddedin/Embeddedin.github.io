# 주변장치 접근

Rust 임베디드 생태계에서는 PAC, HAL, BSP 계층을 나눠 사용하는 경우가 많습니다.
PAC는 레지스터 수준 접근을 제공하고, HAL은 안전하고 추상화된 API를 제공합니다.

1. PAC로 칩 레지스터 정의를 가져옵니다.
2. HAL로 GPIO, 타이머, 통신 장치를 초기화합니다.
3. BSP로 특정 보드의 LED, 버튼, 센서 이름을 사용합니다.

## 계층 구분

| 계층 | 의미 | 예시 |
| --- | --- | --- |
| PAC | Peripheral Access Crate | 칩 레지스터 직접 접근 |
| HAL | Hardware Abstraction Layer | GPIO, UART, SPI 추상화 |
| BSP | Board Support Package | 보드 LED, 버튼, 핀 이름 |
