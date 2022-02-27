<template>
  <div class="main">
      <div class="date">
        <h1 class="title">Atte</h1>
        <div class="header">
          <p class="home"><a href="#">ホーム</a></p>
          <p class="date_page"><a href="date">日付一覧</a></p>
          <p class="logout"><a href="/login">ログアウト</a></p>
        </div>

      </div>
      <div class="table">
        <div class="table-date"><span type="button"  v-on:click="pushedBtnSlider(1)" :class="{ 'button-slider': isPush1 }">＜</span>{{ new Date() | moment }}<span v-on:click="pushedBtnSlider(2)" :class="{ 'button-slider': isPush2 }" >＞</span></div>

         <table>
          <tr>
            <th>名前</th>
            <th>勤務開始</th>
            <th>勤務終了</th>
            <th>休憩時間</th>
            <th>勤務時間</th>
          </tr>

          <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>

        </table>

        <div class="container">
          <div>
            <sliding-pagination
             :current="currentPage"
             :total="totalPages"
               @page-change="pageChangeHandler"
             />
          </div>
        </div>
      </div>






  </div>
</template>


<script>
import moment from 'moment';

export default {
  data() {
    return {
      currentPage: 1,
      totalPages: 100,
    }
  },
  methods:{
      pageChangeHandler (selectedPage) {
      this.currentPage = selectedPage
    },
      pushedBtnSlider(s) {
      if(s === 1){
      console.log(moment.add(1,'d'));
      }
    }
  },
  components: {
  },
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
    width
    /***/
    : auto;
  }

  /* style.css */

  #__nuxt {
    width: 100%;
  }
  .main {
    width: 80%;
    min-width: 608px;
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

  .table span:nth-of-type(1) {
    margin-right: 10px;
    background-color: white;
    color: #2384cf;
    border: 1px solid;
    border-color: #2384cf;
    padding: 0.1em;
    border-radius: 0.2em;
  }

  .table span:nth-of-type(2) {
    margin-left: 10px; 
    background-color: white;
    color: #2384cf;
    border: 1px solid;
    border-color: #2384cf;
    padding: 0.1em;
    border-radius: 0.2em;


  }


  .table {
    width: 100%;
    height: 620px;
    border-spacing: 25px;
    border-collapse: separate !important;
    margin-top: 30px;
    background-color: #f2f2f2;
  }

  .table-date{
    display: block;
    text-align: center;
    font-weight: bold;    
    padding-top: 25px;
  }

  table {
    table-layout: fixed;
    box-sizing: border-box;
    border-collapse: separate !important;
    border-spacing: 80px;
    display: block;
    align-items: center;
  }

  .container {
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .c-sliding-pagination__list-element {
    color: #2384cf;
    background-color: white;
  }

  .c-sliding-pagination__list-element:hover {
    color: #2384cf;
    background-color: white;
    opacity: 0.6;
  }

.c-sliding-pagination__list-element--active {
  color: #2384cf;
  background-color: white;

}
  .small {
    display: block;
    text-align: center;
  }

</style>