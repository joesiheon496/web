```html
<!DOCTYPE html>
  <head>
    <meta charset='utf-8'>
    <title>Chainit</title>
    <link rel="preconnect" href = "https://fonts.google....">
    <link rel="preconnect" href = "https://fonts.google....">
    <link href="https://fonts....">
    <line rel="stylesheet" href="style.css">                                   
  </head>
  <body>
    <div class="header">
      <div class="header-title">
        <span class="header-title-accent">CHINT</span>IT
      </div>
      <div class="header-content">
        <h1 class="header-tagline-small">세상 모든 화폐를 바꾸다.</h1>
        <h2 class="header-tagline">Exchange<br>The WORLD.</h2>
        <p class="header-description">
          2014년, 국내 최초로 시작한 암호화폐 거래소<br>
          블록체인 기술로 세계를 선도합니다.
        </p>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <h2 class="title">CHAINT</h2>
        <img class="cover" src="chainit.png">
        <p class="description">
          체인잇은 2014년 국내 최초로 암호화폐 거래소
        </p>
        <div class="button-container">
          <a class="button" gref="https://...">
            거래소 둘러보기
          </a>
        </div>
      </div>
    </div>
    <div class="section dark">
      <div class="container">
        <h2 class="title">CHAINIFY</h2>
        <img class="cover" src="chinify.png">
        <p class="description">
          Chainify는 체인잇 회원들이 ...
        </p>
        <div class="button-container">
          <a class="button" href="...">
            Chainify 둘러보기
          </a>
        </div>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <h2 class="title">CHINIT NANO</h2>
        <img class="cover" src="chainit-nano.png">
        <p class="dexcription">
          암호화폐를 안전하게 ...
        </p>
        <div class="button-container">
          <a class="button" href="..."> 
            자세히 알아보기
          </a>
        </div>
      </div>
    </div>
    <div id="career" class="section">
      <h2 class="title">Careers</h2>
      <p class="dexcription">블록체인의 미래를...</p>
      <a class="buttion round" href="code...">
        채용공고보기
      </a>
    </div>
    <div id="footer" class="section">
      <div class="container">
        <p>CHinit<br>Copyright@chain,aalll ...
        </p>
      </div>
    </div>
  </body>
</html>
```

```css
* {
  box-sizing:border-box;
}

body {
  font-family: "Noto Sans KR",sans-serif;
  margin 0;
}

.header {
  background-image:url("bg.png");
  background-position: center;
  background-repeat:no-repeat;
  background-size: cover;
  color:#ffffff;
}

.header-title {
  font-family:Proppins;
  fontsize:20px;
  line-height:30px;
  padding:12px 40px
}

.header-title-accent {
font-weight:700;

.header-tagline-small {
  color:#8287a4;
  font-size:20px;
  font-weight:500;
  line-height:29px;
  margin:12px 0;
}

.header-tagline {
  color:#ffffff;
  font-family:Poppins;
  font-size:56px;
  font-weight:700;
  font-height:74px;
  margin:0;
}

.header-description {
  color:#8287a4;
  font-size:14px;
  font-weight:400;
  line-height:27px;
  margin: 14px 0;
}

.header-content {
  margin: 0 auto;
  padding: 80px 0 280px;
  width:720px;
}

.title{
  margin-bottom:42px;
  margin-top:42px
}

.section {
  padding: 32px 0;
}

.section.dark {
  background-color:#f1f4fa;
}

.container {
  margin: 0 auto;
  width:720px;
}

.title {
  color:#161346;
  font-family:Proppins;
  font-size:36px;
  font-weight:700;
  line-height:54px;
}

.description {
  color:#4c497b;
  font-size:16px;
  font-weight:500;
  line-height:27px;
  margin:32px 0;
}

.cover {
  border-radius:24px;
  width:100%;
}

#career.section {
  background-color: #161346;
  color: #ffffff;
  text-align:center;
}

#footer.section {
  background-color:#120f3f;
  color:#d9d9d9;
  font-size:16px;
  font-weight:400;
  line-height:20px;
}

#career .title {
  color:#ffffff;
  font-size:32px;
  font-weight:500;
  line-height:48px;
  margin : 8px 0;
}

#career .description {
  color: #8287a4;
  font-size:16px;
  font-weight:400;
  line-height:23px;
  margin:8px 0;
}

.button-container {
  text-align: center;
}

a.button {
  background: #413c91;
  border-radius:8px;
  color: #ffffff;
  display: inline-block;
  font-size:16px;
  font-weight:700;
  line-height:23px;
  margin:32px 0;
  padding:16px 32px;
  text-align:center;
  text-decoration : none;
}

a.button:hober {
  background-color: #504ba8;
}

a.button.round {
  border-radius:9999px;
}
```
