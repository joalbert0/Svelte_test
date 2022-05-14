<script>
  import Button from "./Button.svelte";
  import Text from "./text.svelte";
  //export let number;
  let a = 'Test'
  let text = ''
  let src = "https://cdn.icon-icons.com/icons2/2596/PNG/512/check_one_icon_155665.png"
let count = 0
let doubled

$: doubled = count * 2; /// valores reactivos
function incrementCount() {
	count += 1;
}

let data = [
		{ id: 'J---aiyznGQ' },
    { id: 'z_AbfPXTKms'},
    { id: 'z_Adgrtdt1'},
	];

</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
	<h1>Hello {a} </h1>
  <img alt="img chk" src={src} width='50'/>

  <button on:click={incrementCount}>
  Clicked {count}</button>

  <p>Doubled {doubled} </p>
  <input type="text" bind:value={text}>
  <p>{text}<p/>
  <Button number={1}/>

  <Text/>
  <Text number={1}/>
  <Text number={3}/>

  {#if count > 2} <!-- render condicional  -->
  
  <p>true</p>
  {:else}
  <p> false </p>
   {/if}

   {#each data as item}
		<li>
			{item.id}
		</li>
	{/each}





</main>