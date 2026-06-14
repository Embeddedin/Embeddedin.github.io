# Embedded Rust Book 스타일 문서

이 문서는 Rust 임베디드 학습 내용을 정리하기 위한 mdBook 기반 문서입니다.
왼쪽에는 장별 목차가 표시되고, 본문은 읽기 좋은 폭으로 구성됩니다.

mdBook을 사용하면 Markdown 파일을 장별로 관리하면서 검색, 테마 전환, 이전/다음 장 이동 같은 문서 기능을 자동으로 얻을 수 있습니다.

> 지금 저장소는 `src/` 아래의 Markdown 파일을 원본으로 사용합니다.
> HTML 결과물은 `mdbook build` 실행 후 `book/` 디렉터리에 생성됩니다.

## 기본 명령

```sh
mdbook serve --open
mdbook build
```

로컬에 `mdbook`이 없다면 다음 명령으로 설치할 수 있습니다.

```sh
cargo install mdbook
```
