<script>
	let names = [];
  
	fetch("http://localhost:3001/prenoms")
	  .then((response) => response.json())
	  .then((data) => {
		names = data;
	  });
  </script>
  
  <style>
	/* Styles pour le titre */
	h1 {
	  color: #fff;
	  font-size: 3rem;
	  text-align: center;
	  margin-bottom: 2rem;
	  text-shadow: 1px 1px 0 #333, -1px -1px 0 #333, 1px -1px 0 #333, -1px 1px 0 #333;
	}
  
	/* Styles pour la liste */
	ul {
	  list-style: none;
	  padding: 0;
	  margin: 0 auto;
	  width: 80%;
	  max-width: 600px;
	}
  
	/* Styles pour chaque élément de la liste */
	li {
	  padding: 1rem;
	  background-color: #333;
	  box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
	  margin-bottom: 1rem;
	  font-size: 1.5rem;
	  text-align: center;
	  cursor: pointer;
	  transition: all 0.2s ease;
	  color: #fff;
	}
  
	/* Styles pour l'animation au survol de la liste */
	li:hover {
	  transform: scale(1.05);
	  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
	  background-color: #fff;
	  color: #333;
	}
  </style>
  
  <!-- Le titre de l'application -->
  <h1>Liste des prénoms</h1>
  
  <!-- La liste des prénoms -->
  <ul>
	{#each names as name}
	  <li>{name}</li>
	{/each}
  </ul>
  