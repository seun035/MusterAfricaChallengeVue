<template>
    <div v-if="result">
        <h1>
            Starwars
        </h1>
        <p>Name: {{result.name}}</p>
        <p>Gender: {{result.gender}}</p>
        <p>Mass: {{result.mass}}</p>
        <p>Height: {{result.height}}</p>
        <p>Hair color: {{result.hair_color}}</p>
        <p>Skin color: {{result.skin_color}}</p>
        <p>Eye color: {{result.eye_color}}</p>
        <p>Home world: {{result.homeworld}}</p>
        <p>Birth year: {{result.birth_year}}</p>
        <p>Created: {{result.created}}</p>
        <p>Edited: {{result.edited}}</p>
        <p>Url: {{result.url}}</p>
        <ul class="result-list">
            Films
            <li v-for="(film, index) in result.films" :key="index">{{film}}</li>
        </ul>
        <ul class="result-list">
            Starships
            <li v-for="(starship, index) in result.starships" :key="index">{{starship}}</li>
        </ul>
        <ul class="result-list">
            Vehicles
            <li v-for="(vehicle, index) in result.vehicles" :key="index">{{vehicle}}</li>
        </ul>
        <ul class="result-list">
            Species
            <li v-for="(specie, index) in result.species" :key="index">{{specie}}</li>
        </ul>
    </div>
</template>

<script>
export default {
   props: {
       result: Object
   } 
}
</script>

<style scoped>
.result-list {
    list-style-type: none;
}
</style>