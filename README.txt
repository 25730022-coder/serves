책방틈 데이터 연결 버전

1. 폴더 구조
- index.html
- css/style.css
- js/app.js
- js/supabase-config.js
- data/bookstores-local.json
- data/bookstores-api.json
- data/places.json
- data/sharedCourses.json
- data/news.json

2. 데이터 연결 방식
- index.html이 js/app.js를 불러옵니다.
- js/app.js가 data/ 폴더의 JSON 파일을 fetch로 읽습니다.
- 책방 데이터 2종은 중복을 정리해 하나의 탐색 목록으로 합칩니다.
- 산책/휴식 장소와 공유 코스는 각각 places.json, sharedCourses.json에서 읽습니다.
- 홈 새소식은 news.json에서 읽습니다.
- 로그인 사용자 개인 데이터(후기, 저장 코스 등)는 기존 Supabase 연결 설정을 사용합니다.

3. 실행 방법
JSON fetch는 브라우저 보안 정책상 index.html을 파일 더블클릭(file://)으로 열면 차단될 수 있습니다.
프로젝트 폴더에서 터미널을 열고 아래 명령으로 로컬 서버를 실행하세요.

Windows:
  py -m http.server 8000

또는:
  python -m http.server 8000

그다음 브라우저에서 http://localhost:8000 을 여세요.

4. 데이터 파일을 수정할 때
data 폴더 안의 JSON 파일을 수정하면 됩니다. 파일명과 JSON 구조는 유지해 주세요.
