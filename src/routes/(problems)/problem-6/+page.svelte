<script>
	let array = [...Array(101).keys()];
	array.splice(0, 1);

	let sumOfSquares = array
		.map((n) => {
			return n * n;
		})
		.reduce((a, b) => {
			return a + b;
		});
	let squareOfSums = Math.pow(
		array.reduce((a, b) => {
			return a + b;
		}),
		2
	);
	console.log(squareOfSums);
	console.log(sumOfSquares);

	let answer = squareOfSums - sumOfSquares;
</script>

<h1>Problem 6</h1>

<p>The sum of the squares of the first ten natural numbers is, 1^2 + 2^2 + ... + 10^2 = 385</p>
<p>The square of the sum of the first ten natural numbers is, (1 + 2 + ... + 10)^2 = 55^2 = 3025</p>
<p>
	Hence the difference between the sum of the squares of the first ten natural numbers and the
	square of the sum is 3025 - 385 = 2640.
</p>
<p>
	Find the difference between the sum of the squares of the first one hundred natural numbers and
	the square of the sum.
</p>

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
