# 프로젝트 구조

임베디드 프로젝트는 보통 `no_std` 환경에서 동작합니다.
운영체제의 표준 라이브러리에 기대지 않고, panic 처리, 메모리 배치, 진입점을 직접 명시합니다.

```rust
#![no_std]
#![no_main]

use cortex_m_rt::entry;
use panic_halt as _;

#[entry]
fn main() -> ! {
    loop {
        // board-specific logic
    }
}
```

일반적인 구성은 다음과 같습니다.

- `Cargo.toml`: 의존성, feature, target별 설정 관리
- `.cargo/config.toml`: 기본 target과 runner 설정
- `memory.x`: 플래시와 RAM 메모리 영역 정의
- `src/main.rs`: 펌웨어 진입점
