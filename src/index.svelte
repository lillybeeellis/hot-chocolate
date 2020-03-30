<script>
let name = ""
let tempC = 20
$: tempF = Math.round ( 1.8 + 32)
 </script>

<h1>Hot Chocolate </h1>

<label>
Name:
<input type="text" bind:value={name}>
</label>


<label>
Drink temperature:
 <input type="range" min="0" max="100" bind:value={tempC}>
</label>

{#if name.length > 0}
 <p>Hi {name}, your drink is {tempC} degrees ({tempF}) degrees fahrenheit.</p>


{#if tempC < 40}
... fairly tepid ❄
{:else if tempC > 90}   ️
... very hot 🔥
{:else}
... looks good ☕️
{/if}

{/if}
