<script>
export default {
    name: 'pokemon card',
    props: {
        name: String,
        image: String,
        numberPokedex: Number,
        type1: String
    }

};
</script>

<template>
    <div class="card bg-secondary-subtle">
        <div class="img-box">
            <img :src="image" :alt="name" class="img-fluid rounded">
        </div>
        <div class="p-2">
            <span>{{ numberPokedex }}</span>
            <h4 class="text-center ">{{ name }}</h4>
            <div class="type">{{ type1 }}</div>
        </div>


    </div>
</template>

<style lang="scss" scoped>
.card {
    height: 100%;



    .type {
        background-color: lightpink;
        font-weight: bold;
        border-radius: 10px;
        padding: 3px 8px;
        width: 45%;
        font-size: 16px;

    }

    span {
        color: gray;
        font-size: 14px;
    }
}
</style>
