<script>
  function handleMouseenter() {
    console.log('Cursor memasuki halaman')
  }

  function handleMouseleave() {
    console.log('Cursor meninggalkan halaman')
  }
</script>

<!-- Memasukan HTML ke dalam tag Head -->
<svelte:head>
  <title>Custom Title</title>
</svelte:head>

<!-- Memasukan / menjalankan fungsi pada tag Body -->
<svelte:body
  on:mouseenter={handleMouseenter}
  on:mouseleave={handleMouseleave}
/>

<!-- Melakukan re-konfigurasi Svelte compiler -->
<svelte:options
  immutable={true}
/>