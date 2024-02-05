<script>
export default {
    name: 'pokemon card',
    props: {
        name: String,
        image: String,
        numberPokedex: Number,
        type1: String,
        type2: String
    }

};
</script>

<template>
    <div class="card bg-secondary-subtle">
        <div class="img-box p-1">
            <img :src="image" :alt="name" class="img-fluid rounded">
        </div>
        <div class="p-2">
            <span>{{ numberPokedex }}</span>
            <h4 class="text-center ">{{ name }}</h4>
            <div class="types d-flex">
                <div class="type me-2">{{ type1 }}</div>
                <div class="type bg-info" v-if="type2">{{ type2 }}</div>
            </div>
        </div>


    </div>
</template>

<style lang="scss" scoped>
.card {
    height: 100%;
    position: relative;

    .img-box {
        height: 200px;
    }

    img {
        height: 200px;
        width: 100%;
    }

    h4 {
        margin-bottom: 50px;
    }

    .type {
        font-weight: bold;
        border-radius: 10px;
        padding: 3px 8px;
        width: 45%;
        font-size: 16px;
        text-align: center;
        background-color: coral;
    }

    span {
        color: gray;
        font-size: 14px;
    }

    .fire {
        background-color: red;
    }
}
</style>
