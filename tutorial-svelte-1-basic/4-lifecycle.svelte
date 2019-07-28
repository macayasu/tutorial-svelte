<script>
  import {
    onMount,
    tick,
    beforeUpdate,
    afterUpdate,
    onDestroy
  } from 'svelte'

  let photos = []

  // Dijalankan setelah halaman di buat
  onMount(async () => {
    const res = await fetch('...')
    photos = await res.json()

    // Menunggu suatu proses yang belum selesai
    await tick()

    // do something here
  })

  // Dijalankan ketika komponen akan di buat
  beforeUpdate(() => {
    // do something here
  })

  // Dijalankan ketika komponen telah di buat dan di sync dengan data
  afterUpdate(() => {
    // do something here
  })

  // Dijalankan setelah komponen di hapus dari halaman
  onDestroy(() => {
    photos = []
  })
</script>