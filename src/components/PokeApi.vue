<script>
export default {
  name: 'PokeApi',
  data() {
    return {
      searchQuery: '',
      pokemon: null
    };
  },
  methods: {
  async fetchPokemon() {
      const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${this.searchQuery.toUpperCase()}`);
      const data = await response.json();
      console.log(data); 
      if (response.status === 200) {
        console.log('Todo ok!');
      } else {
        console.log('Error en fetching!');
      }
      this.pokemon = {
        name: data.name,
        abilities: data.abilities.map(h => h.ability.name),
        moves: data.moves[0].move.name,
        image: data.sprites.front_default
      };
    }
  },
}
</script>

<template>
    <div class="item item-3">
        <input type="text" name="search" id="search-input" placeholder="Busca un Pokemon..." v-model="searchQuery">
        <button class="search-button" @click="fetchPokemon">Buscar</button>
        
        <div v-if="pokemon" class='poke-card'>
          <h3 class="pokename">{{ pokemon.name }}</h3>
          <br>
          <p class="pokeability">Habilidades: </p>
          <br>
          <ul class="pokeability-list" style="list-style-type:disc;">
            <li class="pokelist" v-for="(ability, index) in pokemon.abilities" :key="index">
              {{ ability }}
            </li>
          </ul>      
          <p class="pokemoves">Movimientos: </p>
          <p class="move">{{ pokemon.moves }}</p>
        </div>
        <div v-else class="poke-placeholder">
          <img src="../assets/pokeapi.png" alt="Pokeapimg" class="pokelogo" />
        </div>
        <div v-if="pokemon" class="poke-image">
          <img :src="pokemon.image" alt="Pokemon Image" class="poke-img">
        </div>
      </div>
</template>