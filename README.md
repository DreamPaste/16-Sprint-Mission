# 스프린트 미션 1
## 배포 링크
>
## 요구사항
- 랜딩 페이지의 url path는 루트(‘/’) 입니다.
- title은 “판다마켓”으로 설정해 주세요.
- 화면의 너비가 1920px 이상이면 하늘색 배경색은 너비를 꽉 채우도록 채워지고, 내부 요소들의 위치는 고정되고, 여백만 커지도록 해주세요.
- 화면의 너비가 1920px 보다 작아질 때, “판다마켓” 로고의 왼쪽 여백 200px“로그인" 버튼의 오른쪽 여백 200px이 유지되고, 화면의 너비가 작아질수록 두 요소간 거리가 가까워지도록 해주세요.
- 클릭으로 기능이 동작해야 하는 경우, 사용자가 클릭할 수 있는 요소임을 알 수 있도록 cursor:  pointer를 설정해 주세요.
- “판다마켓” 클릭 시 루트 페이지(‘/’)로 이동시켜주세요.
- “구경하러 가기" 클릭 시 (“/items”)페이지로 이동시켜주세요.(빈 페이지)
- “Privacy Policy”, “FAQ”는 클릭 시 각각 아래 페이지로 이동합니다 - Privacy 페이지(‘/privacy’)  - FAQ 페이지(‘/faq’)
- 사용자의 브라우저가 크고 작아짐에 따라 페이지의 요소간 간격, 요소의 크기, font-size 등 모든 크기와 관련된 값이 크고 작아지도록 설정해 보세요.(설정값은 자유입니다).
-  PC사이즈만 고려해 주어진 디자인을 구현합니다.
HTML, CSS 파일을 Netlify로 배포해 주세요. (참고: https://www.codeit.kr/learn/5309)
페이스북, 트위터, 유튜브, 인스타그램 아이콘은 클릭 시 각각의 홈페이지로 새로운 창이 열리면서 이동 합니다.

## 프로젝트 구조
- /assets
    - /icon
    - /img
    - /logo
- index.html
- style.css

## HTML 구조 및 구현 사항
### 전역 CSS 설정
- `:root` 속성을 활용해 color들을 전역 변수로 지정하여 사용했습니다.
- `@font-face` 속성을 활용해 웹 폰트를 사용합니다.
- `font-size: clamp(12px, 1.6vw, 16px)` 를 통해, 폰트 사이즈가 12px에서 16px 사이로 유연하게 조절됩니다.
- `.pointer` 클래스를 사용하여 사용자가 클릭하는 요소임을 알 수 있습니다.
### HTML 구조
- 크게 header, main, footer 영역으로 나뉘어 있습니다.
- **header**는 `position: fixed` 를 사용하여 상단에 고정되어 있습니다.
- **main**은 각 section들로 구성되어 있고, `.top`, `.bottom`, `.section`으로 나뉩니다.
- 세부 정렬은 대부분 **flexbox**를 활용했습니다. 

### 요구사항 구현
- `.landing` 클래스는 하위 박스인 `.wrap` 에서, `max-width`와 `margin: 0 auto`를 활용해서 하늘색 배경색은 너비를 꽉 채우도록 채워지고, 내부 요소들의 위치는 고정되고, 여백만 커지도록 구현했습니다.
- 링크로 연결되는 항목들은 `<a>`태그로 감싸서, 클릭시 특정 페이지들로 이동할 수 있습니다.
- 폰트, 이미지, 몇몇 여백들은 `vw`를 활용해서 동적으로 크기가 조절됩니다.
- 새 창으로 열리는 페이지들은 `target="_blank" rel="noopener"`속성을 사용하여, 보안상 취약점이 발생하고 퍼포먼스가 저하되는 문제를 해결했습니다.

### 코드 리뷰 요청 사항
- 미디어쿼리를 사용하지 않고 제작하여 화면이 줄어들면 의도치 않은 디자인의 변경이 이루어집니다.
- figma를 기준으로 제작했을때 여백이나 위치 등 css를 어느 수준가지 일치시켜야 하는지 기준이 궁금합니다.
- 코드의 개선이 가능하다면 어떤 점을 개선해야할지 궁금합니다.

