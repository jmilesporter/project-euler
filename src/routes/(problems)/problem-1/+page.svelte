<script>
	let startingPool = [...Array(1000).keys()];

	let additionPool = [];

	let answer = 0;

	for (let i = 1; i < startingPool.length; i++) {
		if (i % 3 === 0 || i % 5 === 0) {
			additionPool.push(i);
		}
	}
	for (let i = 0; i < additionPool.length; i++) {
		answer = answer + additionPool[i];
	}
	console.log(additionPool);
</script>

<h1>Problem 1</h1>
<p>
	If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9.
	The sum of these multiples is 23.
</p>
<p>Find the sum of all the multiples of 3 or 5 below 1000.</p>
<p class="answer">{answer}</p>

<style>
	h1 {
		text-align: center;
		margin: 1.5em;
	}
	p {
		text-align: center;
	}
	.answer {
		text-align: center;
		font-size: xxx-large;
		align-items: center;
	}
</style>
