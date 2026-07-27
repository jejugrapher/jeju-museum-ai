# 앱스크립트 주소가 바뀌었을 때

**작성일:** 2026.07.27

앞으로는 **`app.json` 한 파일만** 고치면 됩니다.
`show/index.html`, `teacher/index.html` 은 다시 올릴 필요가 없습니다.

---

## 순서

1. Apps Script 에서 **배포 → 새 배포** → 새 URL 복사
2. GitHub 저장소 첫 화면에서 **`app.json`** 클릭
3. 오른쪽 위 **연필(Edit this file)** 클릭
4. `exec` 값의 따옴표 안쪽만 새 주소로 교체

```json
{
  "exec": "https://script.google.com/macros/s/새주소/exec",
  "teacherKey": "museum"
}
```

5. 아래 **Commit changes** → **Commit changes**
6. 1~2분 뒤 반영

---

## 강사 화면 열쇠를 바꾸려면

`teacherKey` 값을 바꾸고, Apps Script `Code.gs` 의 `var TEACHER_KEY` 도 같은 값으로 맞추면 됩니다.

```json
"teacherKey": "jgm7q2x"
```
```javascript
var TEACHER_KEY = 'jgm7q2x';
```

---

## 동작 방식

두 페이지는 열릴 때 `app.json` 을 읽어 주소를 가져옵니다.
읽지 못하면 페이지 안에 적혀 있는 주소를 씁니다. 즉 `app.json` 이 없어도 멈추지 않습니다.

읽는 주소에 `?t=시각` 이 붙어 있어 브라우저가 옛 파일을 들고 있지 않습니다.

---

## 지금 들어 있는 주소

```
https://script.google.com/macros/s/AKfycbyzH4CJ-nRyRkDIYejsQHoD_e_gUtQNcbH9tWkC-19Xi8Ap7ahikOt3UTQOWrQPWig9/exec
```

- 아이 화면 → 위 주소 그대로
- 강사 화면 → 위 주소 + `?v=t&k=museum`
