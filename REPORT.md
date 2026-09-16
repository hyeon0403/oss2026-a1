# A1 리포트

- 이름: 김정현
- 학번: 2024402014
- GitHub ID: hyeon0403

## 어디를 둘러봤는지

awesome-nodejs에서 `Command-line apps`, `Command-line utilities`, `Mad science` 카테고리를 둘러봤다.

터미널에서는 다음 검색어를 사용해 관련 패키지를 찾아봤다.

```bash
npm search "terminal color"
npm search "terminal spinner"
npm search "qrcode terminal"

```

---

## 선정한 패키지

### 1. `chalk`

**선정 이유:** 
터미널에 출력되는 글자의 색이나 스타일을 간단하게 변경할 수 있다는 점이 흥미로워서 선택했다.

**이것으로 무엇을 할 수 있을지:**
CLI 프로그램에서 성공 메시지와 오류 메시지를 서로 다른 색으로 표시할 수 있을 것 같다.  
또한 중요한 내용을 굵게 표시하거나 색을 넣어서 터미널 출력을 더 보기 쉽게 만들 수 있을 것 같다.

**확인 결과:**

```
$ npm view chalk version time.modified license dependencies
version = '6.0.0'
time.modified = '2026-07-26T14:51:07.471Z'
license = 'MIT'

$ npm view chalk deprecated

```

**출력을 보고 알게 된 것:**
현재 버전은 `6.0.0`이고 MIT 라이선스를 사용하는 것을 확인했다.  
`deprecated` 명령의 출력이 없었기 때문에 현재 지원 중단으로 표시된 패키지는 아니라는 것을 알 수 있었다.

---

### 2. `ora`

**선정 이유:**
터미널에서도 웹페이지의 로딩 화면처럼 움직이는 스피너를 표시할 수 있다는 점이 신기해서 선택했다.

**이것으로 무엇을 할 수 있을지:**
파일 다운로드처럼 시간이 걸리는 작업을 실행할 때 현재 작업이 진행되고 있다는 것을 사용자에게 보여줄 수 있을 것 같다.  
CLI 프로그램의 진행 상태를 단순한 글자보다 보기 좋게 표현할 때 사용할 수 있을 것 같다.

**확인 결과:**

```
$ npm view ora version time.modified license dependencies
version = '9.4.1'
time.modified = '2026-06-22T12:24:49.363Z'
license = 'MIT'
dependencies = {
  chalk: '^5.6.2',
  'cli-cursor': '^5.0.0',
  'cli-spinners': '^3.2.0',
  'is-interactive': '^2.0.0',
  'is-unicode-supported': '^2.1.0',
  'log-symbols': '^7.0.1',
  'stdin-discarder': '^0.3.2',
  'string-width': '^8.1.0'
}

$ npm view ora deprecated
```

**출력을 보고 알게 된 것:**
현재 버전은 `9.4.1`이고 MIT 라이선스를 사용하고 있었다.  
`chalk`, `cli-spinners`, `log-symbols` 등 여러 패키지를 의존성으로 사용하고 있으며, `deprecated` 출력은 없었다.

---

### 3. `qrcode-terminal`

**선정 이유:**
이미지 파일을 따로 만들지 않고 터미널에서 바로 QR 코드를 출력할 수 있다는 점이 신기해서 선택했다.

**이것으로 무엇을 할 수 있을지:**
웹사이트나 GitHub 주소를 QR 코드로 만들어 휴대폰에서 바로 접속할 수 있게 할 수 있을 것 같다.  
또한 서버 주소나 간단한 문자열을 QR 코드 형태로 다른 기기에 전달할 때도 활용할 수 있을 것 같다.

**확인 결과:**

```
$ npm view qrcode-terminal version time.modified license dependencies
version = '0.12.0'
time.modified = '2022-06-25T05:26:27.931Z'

$ npm view qrcode-terminal deprecated
```

**출력을 보고 알게 된 것:**
다른 두 패키지보다 time.modified 값이 오래되었지만, deprecated 출력은 없었다.
또한 이번 명령의 출력에서는 라이선스와 dependencies 정보가 표시되지 않았다

---

## 설치해본 패키지

```
$ npm install chalk

added 1 package, and audited 2 packages in 3s

1 package is looking for funding
  run `npm fund` for details

found 0 vulnerabilities

$ node try.js
Hello, npm!
SUCCESS
ERROR

```

---

## 막혔던 부분 (채점하지 않음)

`npm view` 명령을 처음 사용해서 출력되는 `version`, `time.modified`, `license`, `dependencies`가 각각 무엇을 의미하는지 헷갈렸다.  
과제 설명과 패키지 정보를 확인하면서 각 항목의 의미를 이해할 수 있었다.

```

```

---

## AI 사용

패키지를 고르는 과정에서 각 패키지의 기능과 활용 방법을 정리하기 위해 ChatGPT를 사용하였다.  
또한 `npm view` 명령의 출력 항목을 해석하고, `try.js`에서 패키지를 실제로 호출하는 방법을 확인하는 데 사용하였다.

---

## 제출 전 확인

- [x] 저장소 이름이 `oss2026-a1`, 공개 범위가 Public
- [x] `git status` 결과가 `nothing to commit, working tree clean`
- [x] `node_modules` 폴더를 지우고 `npm install` → `node try.js` 를 다시 해도 실행됨
- [x] 마지막 커밋을 push함
