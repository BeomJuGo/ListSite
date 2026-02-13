# 아이템 목록 사이트

GitHub + Vercel로 배포하는 간단한 아이템 목록 사이트입니다.

## 기능

- **아이템 목록**: `index.html`의 `ITEMS` 배열에 직접 아이템을 추가/수정
- **카테고리 필터**: 카테고리별로 아이템 필터링 (아이템에서 자동 추출)
- **검색**: 띄어쓰기 무시 검색
- **페이지네이션**: 1페이지당 10개 아이템
- **하단 링크**: `FOOTER_LINK_URL`, `FOOTER_LINK_TEXT`로 설정

## 커스터마이징

### 아이템 추가/수정
`index.html`의 `ITEMS` 배열을 수정하세요 (각 아이템은 `name`과 `category` 필요):
```javascript
const ITEMS = [
  { name: "아이템 1", category: "카테고리명" },
  { name: "아이템 2", category: "카테고리명" },
  // ...
];
```
카테고리는 아이템에서 자동 추출되며, 새 카테고리 추가 시 해당 카테고리 버튼이 자동으로 생성됩니다.

### 하단 링크 변경
`index.html`의 하단 설정을 수정하세요:
```javascript
const FOOTER_LINK_URL = "https://원하는-url.com";
const FOOTER_LINK_TEXT = "표시할 텍스트";
```

## 배포 방법

1. GitHub에 저장소 생성 후 이 프로젝트 push
2. [Vercel](https://vercel.com) 접속 → Import Project → GitHub 저장소 선택
3. 자동 배포 완료
