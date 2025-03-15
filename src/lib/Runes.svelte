<script lang="ts">
	let count = $state(0);

	function increment() {
		count++;
	}

	let nums = $state([0]);

	function addNumber() {
		nums.push(nums.length);
	}

	let sum = $derived(nums.reduce((t, k) => t + k));
</script>

<h1>Count is {count}</h1>

<button class="border" onclick={increment}>Increment</button>

<h1>Numbers: {nums.length} ({nums}), Sum: {sum}</h1>

<button class="border" onclick={addNumber}>Add number</button>
