<script>
let name = ""
let temp = 20
 </script>

<h1>Hot Chocolate </h1>

<label>
Name:
<input type="text" bind:value={name}>
</label>


<label>
Drink temperature:
 <input type="range" min="0" max="100" bind:value={temp}>
</label>

{#if name.length > 0}
 <p>Hi {name}, your drink is {temp} degrees.</p>


{#if temp < 40}
... fairly tepid ❄
{:else if temp > 90}   ️
... very hot 🔥
{:else}
... looks good ☕️
{/if}

{/if}
