<script>
  const Message = 'This is a simple page with Svelte'

  function ShowAlert() {
    alert('This is a simple alert')
  }
</script>

<section class="section-wrapper">
  <h1>Hi There,</h1>
  <p>{Message}</p>

  <button on:click={ShowAlert}>
    Show Alert
  </button>
</section>

<style>
  .section-wrapper {
    color: #888;
  }
</style>

<button disabled>Disabled Button</button>