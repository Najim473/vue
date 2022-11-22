<template>
    <!-- <button @click="$emit('buttonClicked')">{{text}}</button> -->
    <button @click="handleButtonClicked">{{text}}</button>
    <!-- <button>{{props.text}}</button> -->
</template>
<script setup>
const props = defineProps({
    text:{
        type:String,
        default:'No text specified'
    }
})
// console.log(props.text)
const emit = defineEmits(['buttonClicked'])
const handleButtonClicked = ()=>{
    emit('buttonClicked','react')
}
</script>

<!-- <script>
export default{
    props:{
        text:{
            type: String,
            default:'No text specified'
        }
    },
    emits:['buttonClicked']
}
</script> -->