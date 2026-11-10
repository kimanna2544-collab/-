# TOEIC MASTER — 설치 가능한 PWA 시제품

## 포함 기능
- Part 5 자체 제작 문제 30개, 정답 즉시 표시, 해설 및 번역
- 좌우 스와이프 / 이전·다음 버튼
- 북마크 및 학습 진도 기기 내 저장(localStorage)
- Service Worker 오프라인 캐시, PWA manifest 및 아이콘

## 배포하기 (GitHub Pages 예시)
1. 압축파일을 풀어 `toeic-master-pwa` 폴더 안의 **모든 파일**을 GitHub 저장소 루트에 업로드합니다.
2. GitHub 저장소의 Settings → Pages → Build and deployment에서 Deploy from a branch, main, /(root)를 선택합니다.
3. 배포된 `https://...github.io/.../` 주소를 **안드로이드 Chrome**에서 엽니다.
4. Chrome 메뉴(⋮) → **앱 설치** 또는 **홈 화면에 추가**를 누릅니다. 환경에 따라 메뉴 이름이 다릅니다.

## 로컬 테스트
폴더에서 `python -m http.server 8000`을 실행하고 `http://localhost:8000`을 엽니다. `file://`로 HTML을 직접 열면 fetch 및 Service Worker가 정상 작동하지 않습니다. 스마트폰 설치에는 HTTPS 주소가 필요합니다.

## 주의
- 앱은 아직 인터넷에 배포되지 않았습니다. 압축파일 자체를 탭하는 것만으로 PWA 설치가 되지는 않습니다.
- 학습 기록은 **해당 기기의 해당 브라우저 저장소**에만 보관됩니다. 브라우저 데이터를 삭제하면 사라질 수 있습니다.
- 30문제는 실제 기출 복제가 아닌 학습용 자체 제작 문항입니다.
- 새 버전 배포 시 Service Worker CACHE 버전을 올려야 기존 캐시가 갱신됩니다.
