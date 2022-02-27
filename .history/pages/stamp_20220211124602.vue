<template>
  <div class="main">
     <div class="date">
      <h1 class="title">Atte</h1>
      <div class="header">
        <p class="home"><a href="#">ホーム</a></p>
        <p class="date_page"><a href="#">日付一覧</a></p>
        <p class="logout"><a href="#">ログアウト</a></p>
      </div>

    </div>
    <div class="stamp">
      <h2 class="h2">さんお疲れ様です!</h2>
        <div class="form_contents">
          <input class="button-add" type="button" value="勤務開始" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled"
>
          <input class="button-add" type="button" value="勤務終了">
          <input class="button-add" type="button" value="休憩開始">
          <input class="button-add" type="button" value="休憩終了">
        </div>


    </div>
    <small class="small">Atte.inc</small>
  </div> 
</template>

<script>
export default {
  data() {
    return {
      startDisabled:false,
      title: '',
      description: '',
    }
  },methods:{
    clickStart(){
      this.startDisabled=true

    }
  }
}
</script>

<style>
<body>
    <div id="__nuxt"><!----><!----><div id="__layout"><div class="main"><div class="header-title"><h1 class="title">Atte</h1></div> <div class="login_contents"><h2 class="h2">会員登録</h2> <span><span><input id="username" type="text" name="名前" placeholder="名前" class="input-add"> <div class="error"></div></span> <span><input id="email" type="email" name="メールアドレス" placeholder="メールアドレス" class="input-add"> <div class="error"></div></span> <span><input id="password" type="password" name="パスワード" placeholder="パスワード" class="input-add"> <div class="error"></div></span> <span><input id="passwordConfirm" type="password" name="確認パスワード" placeholder="確認用パスワード" class="input-add"> <div class="error"></div></span> <button type="button" disabled="disabled" class="button-add">
      送信
    </button></span></div> <div class="register"><a href="/" class="h3 nuxt-link-active">アカウントをお持ちの方はこちら</a></div></div></div></div><script>window.__NUXT__={config:{_app:{basePath:"\u002F",assetsPath:"\u002F_nuxt\u002F",cdnURL:null}}}</script>
  <script src="/_nuxt/runtime.js"></script><script src="/_nuxt/commons/app.js"></script><script src="/_nuxt/vendors/app.js"></script><script src="/_nuxt/app.js"></script>

</body>

<style>
 /* reset.css */
  @charset "UTF-8";

  html,
  body,
  div,
  span,
  applet,
  object,
  iframe,
  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  p,
  blockquote,
  pre,
  a,
  abbr,
  acronym,
  address,
  big,
  cite,
  code,
  del,
  dfn,
  em,
  img,
  ins,
  kbd,
  q,
  s,
  samp,
  small,
  strike,
  strong,
  sub,
  sup,
  tt,
  var,
  b,
  u,
  i,
  center,
  dl,
  dt,
  dd,
  ol,
  ul,
  li,
  fieldset,
  form,
  label,
  legend,
  table,
  caption,
  tbody,
  tfoot,
  thead,
  tr,
  th,
  td,
  article,
  aside,
  canvas,
  details,
  embed,
  figure,
  figcaption,
  footer,
  header,
  hgroup,
  menu,
  nav,
  output,
  ruby,
  section,
  summary,
  time,
  mark,
  audio,
  video {
    margin: 0;
    padding: 0;
    border: none;
    font-style: normal;
    text-align: left;
    zoom: 1;
  }

  article,
  aside,
  details,
  figcaption,
  figure,
  footer,
  header,
  hgroup,
  menu,
  nav,
  section {
    display: block;
  }

  table {
    border-collapse: collapse;
    font-family: inherit;
  }

  h1,
  h2,
  h3,
  h4,
  h5 {
    font-size: 100%;
    font-weight: normal;
    line-height: 1;
  }

  input,
  textarea,
  select {
    font-family: inherit;
    font-size: 16px;
  }

  input[type="button"],
  input[type="text"],
  input[type="submit"] {
    -webkit-appearance: none;
    border-radius: 0;
  }

  textarea {
    resize: none;
    -webkit-appearance: none;
    border-radius: 0;
  }

  th,
  td {
    border-collapse: collapse;
  }

  table th,
  table td {
    white-space: nowrap;
  }

  ul,
  ol {
    list-style-type: none;
  }

  img {
    vertical-align: text-bottom;
    vertical-align: -webkit-baseline-middle;
    max-width: 100%;
    height: auto;
    width: auto;
  }

  /* style.css */

  .main {
    width: 80%;
    margin: 0 auto;
  }

  .title {
    font-size: 28px;
    font-weight: bold;
  }


  .date {
    display: flex;
    justify-content: space-between;
    margin-top: 10%;
  }

  .header {
    display: flex;
  }

  .header p:not(:nth-last-of-type(1)) {
    margin-right: 15px;
  }

  a {
    text-decoration: none;
    color: black;
  }

  .h2 {
    text-align: center;
    padding-top: 3%;
    margin-bottom: 5%;
  }

  .stamp {
    width: 90%;
    margin: 10% auto;
    background-color: rgb(192, 191, 191);
  }

  .form {
    flex-wrap: wrap;
  }

  .form_contents {
    width: 98%;
    margin: 0 auto;
  }

  .button-add:nth-of-type(3) {
    margin-top: 3%;
  }

  .button-add:nth-of-type(4) {
    margin-top: 3%;
  }


  .button-add {
    width: 47%;
    border: 1px solid grey;
    height: 200px;
    margin: 1%;
    background-color: white;
    color: black;
    font-weight: bold;
  }

  .button-disabled {
    color:lightgray;

  }

  .small {
    display: block;
    text-align: center;
  }


  .button-add:hover {
    background-color: rgb(248, 245, 245);
    transition: 0.7s;
  }
</style>