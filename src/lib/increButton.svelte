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
  $: if (count >= 10) {
	console.log('Le compteur est déjà bien assez élevé !'); 
	count = 9;
	console.log('On va s\'arrêter à ' + count)
  }

  function incrementCount() {
    count += 1;
  }
</script>

<h2>Incrementation</h2>

<button on:click={incrementCount}>
  Clicked {count}
  {count <= 1 ? "time" : "times"}
</button>

<p>Le double de {count} est {double}</p>
