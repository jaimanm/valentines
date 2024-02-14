<script>
  import No from "./lib/No.svelte";
  import Yes from "./lib/Yes.svelte";
</script>

<main class="flex-col justify-center items-center">
  <h1>Happy Valentine's Day!</h1>
  <br />
  <h2 class="text-xl font-bold">Will you be my Valentine?</h2>

  <div class="card flex-row justify-between w-auto">
    <Yes />
    <No />
  </div>
</main>
