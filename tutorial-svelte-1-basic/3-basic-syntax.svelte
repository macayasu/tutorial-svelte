<script>
  // Definisi static variabel
  const picture = 'https://placekitten.com/400/400'
  const string = `this string contains some <strong>HTML!!!</strong>`

  // Definisi dynamic variabel
  let count = 0;
  let name = 'Dunia'

  // Definisi fungsi
  function handleClick() {
    count += 1;
  }

  // Definisi reactive variabel
  $: doubled = count * 2
</script>

<section>
  <!-- Memasukan inputan kedalam variabel -->
  <input bind:value={name}>

  <!-- Mencetak variabel -->
  <h1>Halo {name.toUpperCase()}!</h1>

  <!-- Attribute dinamis -->
  <img src={picture} alt="Cat Picture">

  <!-- Mencetak custom HTML -->
  <p>{@html string}</p>

  <!-- Menjalankan fungsi ketika tombol di tekan -->
  <button on:click={handleClick}>
    <!-- Print statement dengan ternary Operator (kondisi singkat) -->
    Clicked {count} {count === 1 ? 'time' : 'times'} with double {doubled}
  </button>

  <!-- Mencetak tulisan dalam IF-ELSE -->
  {#if count > 10}
    <p>Penghitungan telah melebihi 10</p>
  {:else if count > 8}
    <p>Penghitungan mendekati 10</p>
  {:else}
    <p>Penghitungan belum melebihi 10</p>
  {/if}

  <ul>
    <!-- Mencetak tulisan dalam perulangan -->
    {#each [0, 1, 2] as index}
      <li>Angka ke {index + 1}</li>
    {/each}
  </ul>
</section>