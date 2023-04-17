<script>
  import Button from "../../lib/Button.svelte";
  import Heading from "../../components/Heading.svelte";
</script>

<Heading value="My Counter App">
    <Button />
    <!--le lien ci-dessous redirigera vers la page routée (voir volet de gauche dans vscode)
    >> création d'un dossier (ici otherPage) dans "routes (dossier de routage par défaut de Sveltekit"
    >> il faudra créer un fichier "+page.svelte" pour indiquer la redirection à Svelte -->
    <!--<a href="/otherPage">Autre page</a>-->
</Heading>