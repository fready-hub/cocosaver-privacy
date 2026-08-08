# 개인정보 처리방침 게시용

Play Console은 개인정보 처리방침 **URL**을 요구한다. 앱 저장소는 비공개라
GitHub Pages를 쓸 수 없으므로, 이 폴더를 **공개 저장소**에 올려 Pages로 게시한다.

## 게시 방법

```bash
cd deliverables/privacy-site
git init && git add -A && git commit -m "코코세이버 개인정보 처리방침"
gh repo create cocosaver-privacy --public --source=. --push
gh api -X POST repos/<계정>/cocosaver-privacy/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```

몇 분 뒤 `https://<계정>.github.io/cocosaver-privacy/` 로 열린다.
그 주소를 Play Console **앱 콘텐츠 → 개인정보처리방침**과
스토어 등록정보에 넣는다.

원본은 [`docs/privacy_policy.md`](../../docs/privacy_policy.md)다.
내용을 고치면 `index.html`도 다시 만들어 올린다.
