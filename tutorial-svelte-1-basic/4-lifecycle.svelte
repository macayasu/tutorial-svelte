<script>
  import {
    onMount,
    onDestroy,
    beforeUpdate,
    afterUpdate,
    tick
  } from 'svelte'

	let photos = []

  // Dijalankan setelah halaman di buat
	onMount(async () => {
    const res = await fetch('...')

		photos = await res.json()
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