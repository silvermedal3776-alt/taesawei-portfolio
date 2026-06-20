# 이소백

Hugo로 만든 학업/리서치 포트폴리오 사이트.

## 로컬에서 미리보기

1. [Hugo extended 설치](https://gohugo.io/installation/) (v0.134.3 이상 권장)
2. 이 폴더에서 실행:
   ```bash
   hugo server -D
   ```
3. 브라우저에서 `http://localhost:1313` 접속

## 사이트 구조

왼쪽 사이드바 메뉴:

- **연구 프로젝트** (`content/research/`)
- **학습활동** (`content/study/`)
  - 수행평가 (`content/study/performance/`)
  - 동아리 (`content/study/club/`)
  - 기타활동 (`content/study/etc/`)
- **타임랩스** (`content/timelapse/`)
  - 공부영상 (`content/timelapse/study-video/`)
  - 기타영상 (`content/timelapse/etc-video/`)
- **취미활동** (`content/hobby/`)
  - 시 (`content/hobby/poem/`)
  - 소설 (`content/hobby/novel/`)
  - 독후감 (`content/hobby/review/`)
  - 음악감상 (`content/hobby/music/`)
  - 기타활동 (`content/hobby/etc/`)
- **글** (`content/posts/`)

## 새 글 추가하기

원하는 하위 폴더에 맞춰 명령어를 실행하면 됩니다. 예시:

```bash
hugo new study/performance/글-제목.md
hugo new hobby/poem/글-제목.md
hugo new timelapse/study-video/글-제목.md
```

## 새 연구 프로젝트 추가하기

```bash
hugo new research/프로젝트-이름.md
```

`content/research/` 안에 파일이 생성됩니다. `subjects`, `status`, `summary`를 채우고
본문을 작성한 뒤 `draft: false`인지 확인하세요 (archetype에는 draft 필드가 없어 기본적으로 게시됩니다).

## 배포

`main` 브랜치에 push하면 GitHub Actions가 자동으로 빌드하고
GitHub Pages에 배포합니다. 별도 명령어 실행이 필요 없습니다.

### 최초 1회 설정 (GitHub 저장소에서)

1. 저장소 **Settings → Pages** 이동
2. **Source**를 `GitHub Actions`로 변경
3. `hugo.toml`의 `baseURL`은 이미 `https://silvermedal3776-alt.github.io/taesawei-portfolio/`로 설정되어 있습니다
4. main 브랜치에 push하면 몇 분 내로 사이트가 게시됩니다
