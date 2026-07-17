# SalonDeNature Docs

Salon De Nature 예약 관리 시스템의 원장님·관리자용 운영 매뉴얼입니다.

## 저장소에 올리는 방법

1. GitHub에서 새 Repository를 만듭니다.
   - 권장 이름: `SalonDeNature_Docs`
2. 이 ZIP의 **내용물 전체**를 Repository 루트에 업로드합니다.
3. 기본 브랜치가 `main`인지 확인합니다.
4. 첫 Push 후 GitHub의 **Actions** 탭에서 `Deploy documentation`이 성공했는지 확인합니다.
5. GitHub Repository의 **Settings → Pages**로 이동합니다.
6. **Build and deployment → Source**를 `Deploy from a branch`로 설정합니다.
7. Branch를 `gh-pages`, 폴더를 `/(root)`로 선택하고 저장합니다.

사이트 주소는 일반적으로 다음 형식입니다.

```text
https://<GitHub아이디>.github.io/<Repository이름>/
```

예:

```text
https://OrientingFreeman.github.io/SalonDeNature_Docs/
```

## 로컬 미리보기

Python이 설치되어 있다면:

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

macOS/Linux:

```bash
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

브라우저에서 `http://127.0.0.1:8000`을 엽니다.

## 문서 수정

- 글: `docs/` 아래 Markdown 파일
- 이미지: `docs/assets/screenshots/`
- 좌측 메뉴: `mkdocs.yml`의 `nav`
- 디자인: `docs/stylesheets/extra.css`

`main` 브랜치에 변경사항을 Push하면 GitHub Actions가 사이트를 자동 재배포합니다.

## 공개 전 확인

스크린샷에 실제 고객 이름, 전화번호, 이메일, 예약 내용 또는 매출 정보가 포함되어 있다면 공개 저장소에 올리기 전에 가림 처리하십시오. 운영 매뉴얼을 원장님만 보게 할 목적이라면 Repository를 Private으로 유지하고, GitHub Pages 공개 범위가 계정 요금제와 조직 설정에 맞는지도 확인해야 합니다.
