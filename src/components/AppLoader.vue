<script>

export default {
    name: 'AppLoader',
};



</script>

<template>
    <div class="overlay d-flex justify-content-center align-items-center">
        <div class="text">Loading....</div>
    </div>
</template>

<style lang="scss" scoped>
.text {
    font-size: 50px;
}

.overlay {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-color: lightgreen;
}
</style>
