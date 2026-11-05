# 오늘 뭐 먹지?

월별 제철 재료를 선택하고 저녁 메뉴를 찾아보는 반응형 웹사이트입니다.

## 파일

- `index.html`: 디자인과 JavaScript가 포함된 웹페이지
- `menu.json`: 월별 제철 재료와 예시 레시피 데이터

## 실행

두 파일을 같은 폴더에 두고 HTTP 서버로 실행합니다. Python이 설치되어 있으면 다음 명령을 사용할 수 있습니다.

```sh
python -m http.server 8000
```

브라우저에서 http://localhost:8000 을 엽니다. `fetch('./menu.json')`을 사용하므로 HTML 파일을 직접 더블 클릭하는 대신 서버를 이용하세요.

## 기능

- 1~12월 선택, 첫 화면은 접속 시점의 월 선택
- 제철 재료별 레시피 필터
- 요리 종류와 조리 시간 필터
- 조리 재료와 순서를 담은 레시피 상세 창
- 일치하는 레시피가 없을 때 안내 및 필터 초기화

## 데이터 형식

`seasonal`은 월 번호를 키로 하고 재료 이름 배열을 값으로 가집니다. `recipes`는 레시피 객체 배열이며 `name`, `seasonal`, `months`, `type`, `time`, `servings`, `description`, `ingredients`, `steps`, `photo`를 포함합니다.

현재 메뉴는 예시 데이터이며 사진은 외부 Unsplash 참고 이미지입니다. 실제 요리 완성 모습과 다를 수 있습니다.
