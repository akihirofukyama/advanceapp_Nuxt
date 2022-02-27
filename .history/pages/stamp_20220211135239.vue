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
          <div class="form_content">
          <input class="button-add" type="button" value="勤務開始" @click="clickStart" :class="{ 'button-disabled': startDisabled }" >
          <input class="button-add" type="button" value="勤務終了" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled">
          </div>
          <div class="form_content">
          <input class="button-add" type="button" value="休憩開始" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled">
          <input class="button-add" type="button" value="休憩終了" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled">
          </div>
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
    }
  },methods:{
    clickStart(){
      this.startDisabled=true

    }
  }
}
</script>

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
    width: 90%;
    margin: 0 auto;
  }

  .title {
    font-size: 28px;
    font-weight: bold;
  }


  .date {
    width: 95%;
    display: flex;
    justify-content: space-between;
    margin: 10% auto 0;
  }

  .header {
    display: flex;
    font-weight: bold;
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
    font-weight: bold;
  }

  .stamp {
    width: 100%;
    height: 600px;
    margin: 10% auto 0;
    background-color: #f2f2f2;
  }

  .form {
    flex-wrap: wrap;
  }

  .form_contents {
    width: 98%;
    margin: 0 auto;
  }

  .form_content {
    display: flex;
    justify-content: space-between;
  }

  .form_content:nth-of-type(2) {
    margin-top: 30px;
  }

  .button-add:nth-of-type(1) {
    width: 47%;
    height: 200px;
    margin-left: 40px;
    margin-right: 20px;
    background-color: white;
    color: black;
    border: none;
    font-weight: bold;
  }

  .button-add:nth-of-type(2) {
    width: 47%;
    border: 1px solid grey;
    height: 200px;
    margin-left: 20px;
    margin-right: 40px;
    background-color: white;
    border: none;
    color: black;
    font-weight: bold;
  }

  .button-disabled {
    color:lightgray;

  }

  .small {
    display: block;
    text-align: center;
    font-weight: bold;
    margin-top: 10px;
  }


  
</style>