<script>
  let addition = [1, 2, 3];
  let additionMult = [1, 2, 3, 4];
  let addBegin = [1, 2, 3];
  let addBeginMult = [1, 2, 3];

  let removeLast = [1, 2, 3];
  let removeFirst = [1, 2, 3];
  let removeEl = [1, 2, 3, 4, 5];

  function addElements() {
    addition.push(addition.length + 1);
    addition = addition;
  }

  // fonction addition multiple standard
  function addMultipleElements() {
    //additionMult = [...additionMult, 5, 6, 7];
    additionMult = additionMult.concat([5, 6, 7]);
  }
  // fonction addition multiple améliorée
  /* let lastElement =
    additionMult.length > 0 ? additionMult[additionMult.length - 1] : 4;

  function addMultipleElements() {
    const newElements = [lastElement + 1, lastElement + 2, lastElement + 3];
    additionMult = additionMult.concat(newElements);
    lastElement = newElements[newElements.length - 1];
  } */

  function addElementsToBeginning() {
    //addBegin = [0, ...addBegin];
    addBegin = [0].concat(addBegin);
  }

  function addMultipleElementsToBeginning() {
    addBeginMult = [-3, -2, -1, 0, ...addBeginMult];
    //addBeginMult = [-3, -2, -1, 0].concat(addBeginMult);
  }

  function removeLastElement() {
    //removeLast.splice(-1, 1);
    removeLast = removeLast.slice(0, -1);
  }

  function removeFirstElement() {
    //removeFirst.shift();
    //removeFirst = removeFirst.slice(1);
    removeFirst.splice(0, 1);
    removeFirst = removeFirst; //à garder pour réassigner la valeur de removeFirst
  }

  function removeElements() {
    //removeEl.splice(1, 2);
    //removeEl = removeEl;
    //removeEl = removeEl.filter((val) => val !== 2 && val !== 4);
    // Dans cet exemple, on supprime les valeurs 2 et 4
    removeEl.sort((a, b) => b - a); // Triez les index par ordre décroissant
    for (const i of removeEl) {
      removeEl.splice(i, 1);
      removeEl = removeEl;
    }
  }
</script>

<section>
  <h2 class="text-xl font-bold text-gray-900 mb-4 mt-2">
    Méthodes pour ajouter des éléments
  </h2>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={addElements}>push</button
  >
  <p class="mb-4">{addition}</p>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={addMultipleElements}>push (multiple)</button
  >
  <p class="mb-4">{additionMult}</p>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={addElementsToBeginning}>unshift</button
  >
  <p class="mb-4">{addBegin}</p>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={addMultipleElementsToBeginning}>unshift (multiple)</button
  >
  <p class="mb-4">{addBeginMult}</p>
</section>
<section>
  <h2 class="text-xl font-bold text-gray-900 mb-4 mt-2">
    Méthodes pour supprimer des éléments
  </h2>

  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={removeLastElement}>pop</button
  >
  <p class="mb-4">
    Utiliser la méthode slice de l'objet Array pour créer un nouveau tableau
    sans la dernière valeur:
  </p>
  <p class="mb-4">
    Utiliser la méthode splice de l'objet Array pour supprimer la dernière
    valeur directement dans le tableau
  </p>
  <p class="mb-4">{removeLast}</p>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={removeFirstElement}>shift</button
  >
  <p class="mb-4">
    Utiliser la méthode slice de l'objet Array pour créer un nouveau tableau
    sans la première valeur :
  </p>
  <p class="mb-4">
    Utiliser la méthode splice de l'objet Array pour supprimer la première
    valeur directement dans le tableau
  </p>
  <p class="mb-4">{removeFirst}</p>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mb-4 rounded"
    on:click={removeElements}>splice</button
  >
  <p class="mb-4">
    Utiliser la méthode filter de l'objet Array pour créer un nouveau tableau
    sans les valeurs à supprimer:
  </p>
  <p class="mb-4">
    Utiliser la méthode splice de l'objet Array pour supprimer les valeurs
    directement dans le tableau:
  </p>
  <p class="mb-4">{removeEl}</p>
</section>
