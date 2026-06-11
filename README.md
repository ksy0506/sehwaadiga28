# 2028 대입전형 내비게이터

2028학년도 대입전형 시행계획 기준 — 11개 대학 + 첨단학과 + 메디컬(의·치·한·약·수) + 특수목적대 검색 앱
기능: 대학별 상세 / 전형 비교 / 관심 학생(★담기) / 일정(D-day) / 데이터 관리(JSON 내보내기·가져오기, 변경 이력)

## 배포 방법

### Netlify (GitHub 연결)
1. 이 폴더의 모든 파일을 GitHub 저장소에 업로드 (`netlify.toml` 포함)
2. Netlify → Add new site → Import an existing project → GitHub 저장소 선택
3. 빌드 설정은 `netlify.toml`이 자동 적용됨 (command: `npm run build`, publish: `dist`)
4. Deploy 클릭 → 완료

### GitHub Pages (대안)
1. `.github/` 폴더 포함 전체 업로드
2. 저장소 Settings → Pages → Source를 **GitHub Actions** 선택
3. 자동 빌드·배포

## 업로드 시 주의
- 파일을 **개별 선택**해서 드래그하지 말고, 폴더 구조 그대로 올리세요
- 업로드 후 `package.json` 첫 글자가 `{` 인지 확인 (JS 코드가 들어가 있으면 안 됨)
- 숨김 폴더 표시: Mac `Cmd+Shift+.` / Windows 탐색기 → 보기 → 숨긴 항목

## 데이터 수정
- `src/App.jsx`의 데이터 영역 수정 후 커밋 → 자동 재배포
- 앱 내 "데이터 관리" 탭: 전형·모집단위·대학 추가, 변경 이력 기록, JSON 백업·공유

## 기술 스택
React 18 · Tailwind CSS 3 · Vite 5 · lucide-react
