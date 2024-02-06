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
                <div class="type me-2" :class="this.type1">{{ type1 }}</div>
                <div class="type" v-if="type2" :class="this.type2">{{ type2 }}</div>
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
    }

    span {
        color: gray;
        font-size: 14px;
    }

    .Fire {
        background-color: #FD7D25;
    }

    .Bug {
        background-color: #719F3E;
    }

    .Dark {
        background-color: #707070;
    }

    .Dragon {
        background-color: blue;
    }

    .Eletric {
        background-color: #EED535;
    }

    .Fairy {
        background-color: #FCB8E9;
    }

    .Fighting {
        background-color: #D56722;
    }

    .Flying {
        background-color: lightblue;
    }

    .Ghost {
        background-color: #7B62A3;
    }

    .Grass {
        background-color: #9BCB50;
    }

    .Ground {
        background-color: #FFFF6A;
    }

    .Ice {
        background-color: #51C3E7;
    }

    .Normal {
        background-color: gray;
    }

    .Poison {
        background-color: #B97FC8;
    }

    .Rock {
        background-color: #A38C22;
    }

    .Psychic {
        background-color: #F366B9;
    }

    .Steel {
        background-color: #9DB7B7;
    }

    .Water {
        background-color: #4592C3;
    }
}
</style>
