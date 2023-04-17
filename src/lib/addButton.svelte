<script>
  let numbers = [1, 2, 3, 4];

  function addNumber() {
    //numbers.push(numbers.length + 1);
    numbers = [...numbers, numbers.length + 1];
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<section>
  <h2 class="text-xl font-bold text-gray-900 mb-4 mt-2">Ajoute et additionne</h2>

  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={addNumber}
  >
    Cliquez-moi
  </button>

  <p>{numbers.join(" + ")} = {sum}</p>
</section>
