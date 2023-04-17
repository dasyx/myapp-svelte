<script lang="ts">
    // global styles and scripts
    import "../styles.css";
    // l'ajout du fichier "+layout.svelte" et l'import dans le dossier "routes" permet de globaliser les feuilles de styles
  </script>
  
  <!--ci dessous on pourra inclure le contenu répétitif comme dans le cas présent une barre de navigation
  >> ces éléments seront répétés pour chaque route fille-->
  <nav>
    <a href="/">Home</a>
    <a href="/svelteTraining">Training Playground</a>
  </nav>
  
  <!--l'élément "slot" est utilisé pour montrer le contenu de la page étant donné qu'une page est un composant-->
  <slot />
  