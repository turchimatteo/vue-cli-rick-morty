<template>
    <section>
        <div class="container">
            <div v-if="characters.length > 0" class="row row-cols-2 row-cols-lg-4">
                <CharacterCard v-for="character in characters" :key="character.id" :details="character" />
            </div>
            <Loader v-else />
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import CharacterCard from './CharacterCard';
import Loader from './Loader';

export default {
    name: 'CharactersList',
    components: {
        CharacterCard,
        Loader
    },
    data: function() {
        return {
            characters: [],
        };
    },
    created: function() {
        axios.get('https://api.sampleapis.com/rickandmorty/characters')
        .then((response) => {
            this.characters = response.data;
        });
    }
}
</script>

<style scoped lang="scss">

</style>