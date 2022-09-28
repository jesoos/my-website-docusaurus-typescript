---
sidebar_position: 2
---
# Docusaurus 사용 방법

- 반응이 빨라서 좋다.
- Docusaurus 사용하려는 이유:
  - 보안 상 맥북에서 MS 오피스 문서를 사용하지 못하기 때문에 그 대안으로 사용

## 처음에 문서 작성 방법

- https://tutorial.docusaurus.io/docs/tutorial-basics/create-a-document
  - 프로젝트 자동 생성 시 로컬에서 확인할 수 있는 내용과 동일

## Category

- docs 리렉터리 하위에 디렉터리 생성을 하면 바로 반영됨
- 타이틀을 한글로 변경하려면 추가 파일 생성

  - 생성한 디렉터리 하위에  `_category_.json` 파일명으로 생성(sample - 자동 생성된 md 파일에서 가져와서 가공함

  ```json
  {
    "label": "임시 문서",
    "position": 2,
    "link": {
      "type": "generated-index",
      "description": "임시로 생성한 문서 모음"
    }
  }
  ```

## Nav

`docusaurus.config.js`

## Mark down

- 체크리스트는 기본적으로 안됨

---

Documents are **groups of pages** connected through:

- a **sidebar**
- **previous/next navigation**
- **versioning**

## Create your first Doc

Create a Markdown file at `docs/hello.md`:

```md
# Hello

This is my **first Docusaurus document**!
```

A new document is now available at [http://localhost:3000/docs/hello](http://localhost:3000/docs/hello).

## Configure the Sidebar

Docusaurus automatically **creates a sidebar** from the `docs` folder.

Add metadata to customize the sidebar label and position:

```md
---
sidebar_label: 'Hi!'
sidebar_position: 3
---

# Hello

This is my **first Docusaurus document**!
```

It is also possible to create your sidebar explicitly in `sidebars.js`:

```js
module.exports = {
  tutorialSidebar: [
    'intro',
    // highlight-next-line
    'hello',
    {
      type: 'category',
      label: 'Tutorial',
      items: ['tutorial-basics/create-a-document'],
    },
  ],
};
```
