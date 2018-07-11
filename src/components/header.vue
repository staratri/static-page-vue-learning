<template>
    <header>
        <h1 @click = "updateTitle">
            {{title}}
        </h1>
    </header>
</template>

<script>
export default {
    props : {
        title:{
            type : String
        }
    },
    methods : {
        updateTitle : function(){
            this.$emit('updateInTitle', 'After Click Title')
        }
    }
    
}
</script>

<style scoped>
    header{
        padding: 20px;
        background: lightgreen;
    }
    h1{
        text-align: center;
        color : #222;
    }
</style>


