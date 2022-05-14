<script>
	let count = 0;

	function handleClick() {
	  count += 1;
	}
	//export let number = 23;
</script>

<style>
	button {
	  background: #ff3e00;
	  color: white;
	  border: none;
	  padding: 8px 12px;
	  border-radius: 2px;
	}
</style>

<button on:click={handleClick} number={12}>
  Clicked {count} 
</button>
