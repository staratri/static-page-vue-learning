<template>
  <div>
    <app-header :title= 'title' @updateInTitle= "updateSrcTitle($event)"></app-header>
    <app-mainComponent :ninjas = "ninjas"></app-mainComponent>
    <app-footer :title = 'title'></app-footer>
  </div>
</template>

<script>
import Header from './components/header.vue'
import Footer from './components/Footer.vue'
import MainComponent from './components/MainComponent.vue'

export default {
  components : {
    'app-footer' : Footer,
    'app-header' : Header,
    'app-mainComponent' : MainComponent
  },
  data () {
    return {
      ninjas: [
                    {name: 'Ryu', speciality: 'Vue Components', show: false},
                    {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
                    {name: 'Hitoshi', speciality: 'Click Events', show: false},
                    {name: 'Tango', speciality: 'Conditionals', show: false},
                    {name: 'Kami', speciality: 'Webpack', show: false},
                    {name: 'Yoshi', speciality: 'Data Diggin', show: false}
            ],
      title : "Vue JS Practice"
    }
  },
  methods : {
    greeting : function (){
      return 'Heyyy boooouy'
    },
    updateSrcTitle : function (updatedTitle){
      this.title = updatedTitle
    }
  }
}
</script>

