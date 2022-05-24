<template>
    <div>
        <button v-on:click="updateTitle">Update Parent Title</button>
    </div>
</template>

<script>
export default{
    name:'Child_parent',
    methods:{
        updateTitle(){
            this.$emit('changeTitle','Parent Updated')
        }
    }

}
</script>