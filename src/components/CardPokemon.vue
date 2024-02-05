<script>
export default {
    name: 'pokemon card',

};
</script>

<template>
    <div class="card bg-secondary-subtle">
        <div>
            <img src="https://img.pokemondb.net/artwork/large/charizard.jpg" alt="pokemon" class="img-fluid rounded">
        </div>
        <div class="p-2">
            <span>#001</span>
            <h4 class="text-center ">Charizard</h4>
            <div class="type">Fuoco</div>
        </div>


    </div>
</template>

<style lang="scss" scoped>
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
