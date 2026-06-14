# Embedded In Book

mdBook 기반 Rust Embedded 문서입니다.

## 로컬 실행

```sh
cargo install mdbook
mdbook serve --open
```

## 빌드

```sh
mdbook build
```

빌드 결과는 `book/` 디렉터리에 생성됩니다.

## GitHub Pages 배포

이 저장소는 GitHub Actions로 mdBook을 빌드하고 GitHub Pages에 배포합니다.

1. GitHub 저장소의 `Settings` → `Pages`로 이동합니다.
2. `Build and deployment`의 `Source`를 `GitHub Actions`로 설정합니다.
3. `main` 브랜치에 push하면 `.github/workflows/pages.yml`이 `mdbook build`를 실행합니다.
4. 생성된 `book/` 디렉터리가 GitHub Pages에 배포됩니다.
