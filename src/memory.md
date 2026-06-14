# 메모리와 링커

bare-metal 프로그램은 플래시와 RAM 위치를 링커 스크립트로 지정합니다.
보드의 데이터시트를 기준으로 메모리 영역을 정확히 잡아야 플래싱과 실행이 정상적으로 이뤄집니다.

```ld
MEMORY
{
  FLASH : ORIGIN = 0x08000000, LENGTH = 256K
  RAM   : ORIGIN = 0x20000000, LENGTH = 40K
}
```

메모리 설정을 바꿀 때는 다음을 함께 확인합니다.

- 실제 칩의 flash/RAM 시작 주소
- 부트로더가 사용하는 영역
- 스택과 힙 크기
- interrupt vector table 위치
