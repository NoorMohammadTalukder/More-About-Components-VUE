<template>
    <ul>
        <li v-for="goal in goals" :key="goal">
            <!-- {{goal}} -->
        <slot :item="goal"></slot>
        </li>
    </ul>
</template>

<script>
    export default{
        data(){
            return{
                goals:["Goal no 1","Goal no 2"]
            }
        }
    }
</script>
