# CSS 선택자(CSS Selector)
CSS 규칙에서 맨 앞에 적어 주는 걸 CSS 선택자라고 부른다. 선택자를 이용해서 이 규칙을 어떤 요소들에 적용할지 선택할 수 있다.
```css
선택자 {
  선언;
  선언;
  선언;
}
```

# 선택자 목록
콤마`(,)`로 선택자를 연결하면 여러 선택자에 같은 규칙을 적용할 수 있다.
```css
선택자1,
선택자2 {
  ...
}
```

# 선택자 붙여 쓰기
여러 조건을 동시에 만족하는 요소를 선택하고 싶다면 선택자를 붙여서 쓸 수 있다. 예를 들어 아래 HTML 코드에 있는 태그를 선택해본다
```html
<h2 id="mongolia" class = "large title">몽공 대자연으로 떠나는 여행</h2>
```
## 예시1. 아이디+클래스
```css
#mongolia.title
```
## 예시2. 클래스+클래스
```css
.large.title
```
## 예시3. 태그+아이디+클래스
```css
h2#mongolia.large.title
```
# 자식 결합자(child combinator)
오른쪽 꺾쇠로 선택자를 이어준다. 예를 들어 아래 코드에서 tesla-y-2025.png를 보여주는 이미지 태그를 선택하려면 `.article > img`로 선택할 수 있다.
```html
<div class="article">
  <img src="tesla-y-2025.png">
</div>
```
```css
.article > img{
  width:100%;
}  
```
# 자손 결합자(Descendant Combinator)
```css
.article img {
  width:100%;
}  
```
# 가상 클래스 (Pseudo-class)
가살 클래스는 의사 클래스, 가짜 클래스라고도 불린다. 요소의 ㅅ아태 같은걸 선택할 때 사용하는 클래스이다. 정해진 이름 앞에 콜론(`:`)을 붙여서 사용한다. 대표적으로 `:hover`(마우스를 올렸을 때), `:active`(클릭한 상태), `visited`(방문한적이 있는 링크), `focus`(포커싱 됏을 때) 등이 있다. 예를 들어서 밑줄이 없는 링크에 마우스를 올렸을 때 밑줄이 생기도록 하려면 `:hover`를 활용하면 된다.
```css
a {
  text-decoration:none;
}

a:hover {
  text-decoration:underline;
  }
```
# 레슨에서는 자주 쓰지는 않지만 알고 있다면 유용한 선택자
#전체 선택자(Universla selector)
`*`라는 선택자는 모든 요소를 선택하는 선택자이다.

<b>모든 요소를 선택하기</b>
```css
* {
  box-sizing:vorder-box;
  }
```

<b>`.gallery`의 모든 자식 요소 선택하기</b>
```css
.gallery > * {
  width: 120px;
  height: 90px;
  }
```
# n번째 자식 선택자(n-th child Selector)
`:nth-child()`를 사용한다. 괄호 안에는 숫자나 `even`,`odd`,`2n`같은 값이 들어갈 수 있는데 여기서는 1부터 시작한다.(첫번째 자식1)

## `.gallery`의 세번째 자식
```css
.gallery:nth-child(3){...}
```
## `.gallery`의 짝수 번째 자식
```css
.gallery:nth-child(even){...}
.gallery:nth-child(2n){...}
```
# `.gallery`의 홀수 번째 자식
```css
.gallery:nth-child(odd){...}
.gallery:nth-child(2n+1){...}
```
# 특히 첫번째 자식, 마지막 자식은 아래처럼 선택한다.
```css
.gallery:first-child {...}
.gallery:last-chile{...}
```

# 선택자는 최대한 단순하게
앞에서 다양한 선택자와 조합 방법을 배웠는데 클래스, 가짜 클래스 한 두 개만 조합해서 최대한 단순하게 쓰는것을 추천한다. 복잡하게 조합하면 나중에 코드를 고칠 때 어디서 뭐가 바뀔지 알기 힘들다.

그래도 선택자를 조합해서 사용하면 유용한 경우가 있는데 몇가지 예시를 들어주신다.

# 모든 곳에서 border-box를 쓰고 싶을 때
앞에서 박스 모델의 크기는 기본적으로 콘텐트(`content-box`)를 기준으로 정해진다고 배웠다. 모든 요소의 크기를 테두리(`border-box`)를 기준으로 하고 싶다면, 아래처럼 추가하고 사용하면 된다. 항상 이 코드를 추가하는 것도 좋다.
```css
* {
  box-sizing:border-box;
}
```

# 같은 클래스지만 변화를 주고 싶을 때
똑같은 상품 버튼이지만, 품절된 상품의 버튼을 보여줄 때나 똑같은 이미지이지만 유저가 선택한 이미지를 보여줄 때처럼 같은 클래스이지만 살짝 다른 경우에 사용하면 좋다.

예를 들어서 아래 예시는 홈페이지의 메뉴를 만든 것인데, 똑같은 `menu-link`클래스지만, 현재 보고있는 페이지가 소개 경우라서 해당 메뉴만 `selected`클래스를 추가로 넣었다.
```html
<div class="menu">
  <a class="menu-link" href="/">메인</a>
  <a class="menu-link selected">소개</a>
  <a class="menu-link" href="/blog">글</a>
</div>
```
```css
.menu {
  background-color:#000000;
  padding:16px;
.menu-link {
  color: #ffffff;
  font-weight:bold;
  text-decoration:none;
  }
.menu.link.selected,
.menu.link:hover {
  color:#aaaaaa;
}
```
# 클래스 넣어 줄 태그가 너무 많을 때
자손 조합자는 적용해야 할 태그가 너무 많아서, 일일이 적용하기 어려울 때 쓰면 좋습니다. 예를 들어서 아래 코드에서 `<a>`태그에다가 전부 클래스를 추가하기보다는 자손 조합자를 쓰는 게 훨씬 효율적입니다. 여기서 자식 조합자(`.info >a`)를 쓰지 않고 자손 조합자를 쓴 것도 참고해 주세요. 만약에 `<a>` 태그 위치가 `<div>`안에서 자식이 아니라 자손으로 바뀌어도 그대로 동작한다.

```css
.info a {
  color:#379379;
  text-decoration:none;
  }
```

# 가로 마진을 일정하게 하고 싶을 때
이 내용은 종이랑 연필을 가지고 와서 직접 그려보면서 생각해 보면 좋음, 앞에서 마진 상쇄(Margin Collapsing)에 대해 배웠는데 쉽게 말해서 "세로 마진은 겹친다"라는 규칙이 있었음, 예를 들어서 세로로 `article`이라는 클래스의 `<div>` 태그를 배치하고, 세로 마진을 `24px`로 준다고 가정하면 `<dic>`태그는 블록 요소니까 위에서부터 아래로 배치됨
```html
<div class="article">
  하나
</div>
<div class="article">
  둘
</div>
<div class="article">
  셋
</div>
```
```css
.article {
margin:24px 0;
background-color:#ededed;
}
```
그러면 세로 마진은 겹치니까 `article`사이의 간격은 `24px`가 되는데 만약에 세로가 아니라 가로 배치가 된다면?

```html
<span class="chip">섬</span>
<span class="chip">해변</span>
<span class="chip">오두막</span>
```
```css
.chip {
  background-color:#dedede;
  text-align:center;
  display:inline-block;
  width:100px;
  padding:16px;
  margin: 0 24px;
  border-radius:9999px;
}
```
가로로 `24px`만큼씩 여백이 생기는데, 가로 마진은 안겹치니까 `chip`과 `chip`사이에는 24더하기 24, 총 `48px`만큼 간격이 생긴다. 만약에 일정하게 가로로 전부 `24px`로 주고싶다면

`margin-left`(왼쪽 마진), `margin-right`(오른쪽 마진)라는 속성과 함께 `:first-child`나 `:last-child`를 활용하면 좋다.

```css
.chip:first-child {
  margin-left: 24px;
}
```

  















