<script>
import CardPokemon from './CardPokemon.vue';
export default {
    name: 'AppMain',
    components: { CardPokemon },

};
</script>

<template>
    <main class="d-flex align-items-center justify-content-center">
        <div class="row-container">
            <div class="row row-cols-2 row-cols-md-3 row-cols-xl-5 row-cols-xxl-6  gap-4 justify-content-center">
                <div class="col">
                    <CardPokemon />
                </div>
            </div>


        </div>

    </main>
</template>

<style lang="scss" scoped>
main {
    height: 100%;
}

.row-container {
    width: 80%;
    height: 800px;
    background-image: url('https://wallpapercave.com/wp/wp3170189.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    border: 1px solid lightgreen;
    overflow-y: auto;
}

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
</style>
