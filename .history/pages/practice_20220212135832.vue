<template>
  <div class="main">
  <div id="main-panel" class="content-ground p-0 m-0">
    <div class="content-base d-flex p-1 border border-dark">
      <div id='quest-container' class="content-ground p-0 m-0">
        <b-container class="content-main border border-dark">
          <panel01></panel01>
          <panel02></panel02>
          <panel03></panel03>
        </b-container>
      </div>
      <ul class="d-inline">
        <li>
          <button id="push-btn-1" class="btn"
                  v-on:click="pushedBtn(1)" :disabled="isPush1">button 1</button>
        </li>
        <li>
          <button id="push-btn-2" class="btn"
                  v-on:click="pushedBtn(2)" :disabled="isPush2">button 2</button>
        </li>
        <li>
          <button id="push-btn-3" class="btn"
                  v-on:click="pushedBtn(3)" :disabled="isPush3">button 2</button>
        </li>
      </ul>
    </div>
  </div>    

  </div>
</template>

<script>
export default {
  data() {
    return {
  isPush1: false,
      isPush2: false,
      isPush3: false,    }
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

  /* index css */


    .title {
    font-size: 28px;
    font-weight: bold;
    width: 80%;
    margin: 10% auto 0;

  }

  .main {
    margin-top: 10%;
  }

  .h2 {
    text-align: center;
    margin-bottom: 30px;
    font-weight: bold;
    font-size: 18px;
  }

  .login_contents {
    height: 620px;
    background-color: #f2f2f2;
    margin-top:60px ;
  }

  .login_content {
    padding-top:60px ;
  }

  .form {
    width: 70%;
    margin: 0 auto;
  }

  input {
    border-radius: 4px;
  }

  .input-add {
    width: 330px;
    height: 35px;
    display: block;
    margin: 0 auto 30px;
    padding: 5px;
    border-radius: 2px solid;
    background-color: #f2f2f2;


  }

  .button-add {
    width: 340px;
    height: 45px;
    display: block;
    margin: 0 auto;
    background-color: #244ce4;
    color: white;
    border: 1px solid;
    border-radius: 2px solid;
    cursor: pointer;
    outline: none;
    padding: 0;
    appearance: none;
  }

  .h3 {
    display: block;
    margin-top: 10px;
    color: gray;
    text-align: center;
  }

  .register {
    text-align: center;
    font-size: 12px;

  }

  .register_link {
    color: #244ce4;

  }

  .register a {
    text-decoration: none;
  }

  .small {
    margin-top: 10px;
    display: block;
    text-align: center;
    font-weight: bold;
  }

  .error {
    text-align: center;
    margin-bottom: 10px;
  }


</style>