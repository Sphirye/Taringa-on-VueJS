<template>
	<div>
		<div class="cl_header">
			<button v-on:click="showSideBar">Mostrar</button>
			<div class="cl_headLogo">Taringa!</div>
			<div class="cl_headItem">Home</div>
			<div class="cl_headItem">Global</div>
			<div class="cl_headItem">Juegos</div>
			<input class ="cl_headSearcher" type="text" placeholder="Buscar">
			<div class="cl_headSignItem">Registrarme</div>
			<div class="cl_headLogItem">Iniciar sesión</div>
		</div>

		<div class="cl_sideBar cl_sideBarHidden" id="sideMenu">
			<div class="cl_sideBarItems" v-for="item in items" v-on:click="action(item.action)">
				{{ item.title }}
			</div>
		</div>
	</div>
</template>

<style>
/*Sidebar*/
.cl_sideBar{
	border: 1px solid black;
	margin-left: 0px;
	display: flex;
	width: 200px;
	height: 100%;
	flex-wrap: wrap;

	position: fixed;
	transition-delay: 0s;
	transition-duration: 0.5s;
}

button{
	height: 40px;
	margin-left: 10px;
}

.cl_sideBarItems{
	margin-top: 10px;
	width: 100%;
	height: 30px;
	flex-wrap: wrap;
	display: flex;
	justify-content: center;
	align-items: center;
}

.cl_sideBarHidden{
	margin-left: -200px;
}

/*Header*/
.cl_header{
	border: 1px solid orange;
	width: 100%;
	height: 50px;
	
	display: flex;
	flex-direction: row;
	align-items: center;
}

.cl_headItem{
	border: 1px solid orange;
	padding: 10px 20px;
	margin: 0px 5px;
}

.cl_headLogo{
	width: 100px;
	text-align: center;
}

.cl_headSearcher{
	width: 80px;
	height: 40px;
	border-radius: 5px;
	border-style: none;
	background-color: orange;
	padding: 0px 20px;
	margin-right: 190px;
}

.cl_headSignItem{
	border: 1px solid orange;
	height: 40px;
	padding: 0px 10px;
	border-radius: 10px;
	align-items: center;
	display: flex;
	margin-right: 5px;
}

.cl_headLogItem{
	border: 1px solid orange;
	height: 40px;
	padding: 0px 10px;
	border-radius: 10px;
	align-items: center;
	display: flex;
}
</style>

<script>
export default {
	data() {
	    return {
	        items: [
	        //action para añadir acciones
	            {
	                title: 'Conocé Taringa!',
	            },
	            {
	                title: 'Shouts',
	            },
	            {
	            	title: 'Posts',
	            },
	            {
	            	title: 'Tops',
	            },
	            {
	            	title: 'Explorar'
	            },
	            {
	            	title: 'Canales populares'
	            },
	            {
	            	title: 'Hazlo tú mismo'
	            },
	            {
	            	title: 'Humor'
	            },
	            {
	            	title: 'Juegos online'
	            },
	            {
	            	title: 'Recetas y cocina'
	            },
	            {
	            	title: 'Reviews'
	            },
	            {
	            	title: 'Turismo'
	            }
	        ]
	    }
	},
	methods: {
		action(name){
			sideMenu.classList.toggle('cl_sideBarHidden');
		},
		showSideBar(){
			const sideMenu = document.getElementById('sideMenu');

			sideMenu.classList.toggle('cl_sideBarHidden');
		}
	}
}
</script>


