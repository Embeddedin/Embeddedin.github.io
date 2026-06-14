# 빌드와 디버깅

개발 중에는 짧은 피드백 루프가 중요합니다.
`cargo check`로 타입 오류를 빠르게 잡고, 실제 보드에서는 `probe-rs run` 또는 IDE의 디버그 구성을 통해 플래시와 로그를 확인합니다.

```sh
cargo check --target thumbv7em-none-eabihf
probe-rs run --chip STM32F303VCTx target/thumbv7em-none-eabihf/debug/blink
```

## 점검 순서

1. target triple이 보드와 맞는지 확인합니다.
2. probe가 운영체제에서 인식되는지 확인합니다.
3. 칩 이름이 `probe-rs`에서 지원되는지 확인합니다.
4. release/debug 프로파일 차이로 타이밍 문제가 생기지 않는지 확인합니다.
