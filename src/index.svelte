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

<p>Hi {name}, your drink is {temp} degrees.</p>