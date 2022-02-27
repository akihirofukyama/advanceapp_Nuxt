<template>
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
</template>

<script>
// childrens
import Panel01 from './component/Panel01.vue'
import Panel02 from './component/Panel02.vue'
import Panel03 from './component/Panel03.vue'

export default {
  name: 'main-panel',
  components: {
    Panel01, Panel02, Panel03
  },
  data: () => {
    return {
      isPush1: false,
      isPush2: false,
      isPush3: false,
    }
  },
  methods: {
    pushedBtn (s) => {
      if(s === 1){
        this.isPush1 = false;
        this.isPush2 = true;
        this.isPush3 = true;
      } else if ( s === 2) {
        this.isPush1 = true;
        this.isPush2 = false;
        this.isPush3 = true;
      } else if ( s === 3) {
        this.isPush1 = true;
        this.isPush2 = true;
        this.isPush3 = false;
      }
    }
  },
  created() {
    console.log(this)
  }
}
</script>