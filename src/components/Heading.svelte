<script>
  export let value;
  // aucun valeur assignée à la variable ici puisque l'on va pouvoir donner des informations lorsque le composant sera utilisé (grâce à la balise "slot") 
</script>


  <h1 class="text-center">{value}</h1>
  <slot />
  <!--la balise slot permet d'insérer du contenu à l'intérieur du composant-->
