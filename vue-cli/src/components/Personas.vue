<template>
	<div>
		<template v-if="persona">
			<h1 v-text="datosPersona.nombre"><h1>
			<h4 v-text="datosPersona.correo"><h4>
			<img :src="datosPersona.foto">
		</template>
		<span v-else>Cargando informacion, espere......</span>
	</div>
</template>

<script>

import axios from 'axios';

export default{
	mounted(){
		axios.get('https://randomuser.me/api/')
		 .then((response) => {
			this.persona = response.data.results[0];
			console.log(this.persona.name.first);
		})
	},
	data(){
		return {
			persona: null,
		}
	},
	computed: {
		datosPersona(){
			return {
				// nombre: `${this.persona.name.first} ${this.persona.name.last}`,
				nombre: this.persona.name.first,
				foto: this.persona.picture.large,
				correo: this.persona.email,
			}
		}
	}
};

</script>

<style>

</style>