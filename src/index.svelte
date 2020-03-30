<script>
  let name = "";
  let tempC = 20;
  $: tempF = Math.round(1.8 + 32);
</script>

<section class="hero is-primary">
  <div class="hero-body">
    <div class="container">
      <h1 class="title">
        Hot Chocolate
      </h1>
      <h2 class="subtitle">
        How hot do you like your hot chocolate?
      </h2>
    </div>
  </div>
</section>

<section class="section">
  <label class="label">
    Name:
    <input class="input" type="text" bind:value={name} />
  </label>

  <label class="label">
    Drink temperature:
    <input class="input" type="range" min="0" max="100" bind:value={tempC} />
  </label>

  {#if name.length > 0}
    <p>Hi <strong>{name}</strong>, your drink is <strong>{tempC}°C </strong>({tempF})°F.</p>

    {#if tempC < 40}
      ... fairly tepid ❄
    {:else if tempC > 90}️ ... very hot 🔥{:else}... looks good ☕️{/if}
  {/if}

</section>
