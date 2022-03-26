<!-- Please remove this file from your project -->
<template>

<div>
    <p>Test Component 1234</p>
    <p> {{ header }} </p>
</div>

</template>

<script>
export default {

    props:{
        header: String
    },
    
    data() {
        return {
            // header: this.header
        }
    }
}
</script>
