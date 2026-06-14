# 개발 환경

임베디드 Rust 개발은 보통 stable Rust, target toolchain, probe 도구, 그리고 보드별 HAL crate 조합으로 시작합니다.
Cortex-M 계열을 기준으로 하면 다음과 같은 흐름이 일반적입니다.

```sh
rustup target add thumbv7em-none-eabihf
cargo install probe-rs-tools
cargo new blink
cd blink
```

## 권장 도구

| 도구 | 역할 | 메모 |
| --- | --- | --- |
| `rustup` | Rust toolchain 관리 | 타깃 아키텍처 추가에 사용 |
| `cargo` | 빌드와 의존성 관리 | 일반 Rust 프로젝트와 동일 |
| `probe-rs` | 플래싱과 디버깅 | 여러 디버그 프로브 지원 |
