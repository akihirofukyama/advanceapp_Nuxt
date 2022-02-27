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
          <input class="button-add" type="button" value="勤務開始" @click="clickStart()" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled">
          <input class="button-add" type="button" value="勤務終了" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled" >
          <input class="button-add" type="button" value="休憩開始" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled" >
          <input class="button-add" type="button" value="休憩終了" @click="clickStart" :class="{ 'button-disabled': startDisabled }" :disabled="startDisabled">
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
