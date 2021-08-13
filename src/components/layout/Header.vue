<template>
    <div>

  <nav class="navbar navbar-dark bg-dark">
    <div class="container-fluid">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
    </div>
    </nav>

    <div class="collapse" id="navbarToggleExternalContent">
    <div class="bg-dark p-4">
    <div class="service-name">
        <router-link to="/">Open-weather</router-link> |
        <router-link to="/about">Tremendous Weather</router-link>
    </div>
		

     </div>
    </div>


    </div>
</template>

<script>
export default {
  name: 'Header',
  
}
</script>

<style scoped>


.service-name {
			color: white !important;
			text-decoration: none;
			font-size: 20px !important;
		}  
		.service-name :hover{
			color: red !important;
		} 
</style>