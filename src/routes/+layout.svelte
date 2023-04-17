<script lang="ts">
    // global styles and scripts
    import "../styles.css";
    import "../script.js";
    // l'ajout du fichier "+layout.svelte" et l'import dans le dossier "routes" permet de globaliser les feuilles de styles ainsi que les scripts utilisés
    // 
  </script>
  
  <!--ci dessous on pourra inclure le contenu répétitif comme dans le cas présent une barre de navigation
  >> ces éléments seront répétés pour chaque route fille-->
  <nav>
    <a href="/">Home</a>
    <a href="/posts">Posts</a>
  </nav>
  
  <slot />
  