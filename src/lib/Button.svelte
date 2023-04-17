<script>
  let count = 0;
  $: double = count * 2;
  // la notation "$" est utilisée pour définir une exporession réactive qui sera recalculée chaque fois que l'une des variables qu'elle utilise est mise à jour

  // cette notation peut également être utilisée pour déclencher du code côté client, qui sera exécuté chaque fois que la variable qu'elle utilise est mise à jour
  $: {
    //console.log(`Le compteur est maintenant à ${count}`);
	console.log('Le compteur est maintenant à ' + count);
    //alert(`Le compteur est maintenant à ${count}`);
  }

  function incrementCount() {
    count += 1;
  }
</script>

<button on:click={incrementCount}>
  Clicked {count}
  {count <= 1 ? "time" : "times"}
</button>

<p>Le double de {count} est {double}</p>
