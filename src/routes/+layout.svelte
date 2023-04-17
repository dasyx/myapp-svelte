<script>
  // global styles and scripts
  import "../assets/tailwind.css";
  // l'ajout du fichier "+layout.svelte" et l'import dans le dossier "routes" permet de globaliser les feuilles de styles
</script>

<!--ci dessous on pourra inclure le contenu répétitif comme dans le cas présent une barre de navigation
  >> ces éléments seront répétés pour chaque route fille-->
<nav>
  <a href="/">Accueil</a>
  <a href="/svelteTraining">Entrainement & tests</a>
</nav>

<!--l'élément "slot" est utilisé pour montrer le contenu de la page étant donné qu'une page est un composant-->
<slot />
