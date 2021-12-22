<template>
    <div class="character text-center">
        <div class="character-image">
            <img :src="details.image" :alt="details.name">
        </div>

        <div class="character-name">{{ details.name }}</div>

        <div class="character-origin">{{ details.origin }}</div>

        <div class="character-species">{{ details.species }}</div>
    </div>
</template>

<script>
export default {
    name: 'CharacterCard',
    props: {
        details: Object
    }
}
</script>

<style scoped lang="scss">
.character {
    margin-bottom: 50px;

    &-image {
        img {
            border-radius: 50%;
        }
    }

    &-name {
        font-size: 25px;

        &::after {
            content: "";
            width: 45px;
            height: 1px;
            background-color: black;
            display: block;
            margin: 15px auto;
        }
    }

    &-species {
        font-weight: 700;
    }
}
</style>