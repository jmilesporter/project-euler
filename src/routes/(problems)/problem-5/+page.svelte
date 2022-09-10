<script>
	function smallestDivisible(number) {
		for (let i = 2520; i < 10000000000; i = i + 2520) {
			let isDivisible = 0;
			for (let j = 1; j <= number; j++) {
				if (i % j !== 0) {
					break;
				} else {
					isDivisible++;
					console.log(`this is the number: ${i}`);
					console.log(isDivisible);
					if (isDivisible === number) {
						return i;
					}
				}
			}
		}
	}

	let answer = smallestDivisible(20);
</script>

<h1>Problem 5</h1>

<p>
	2520 is the smallest number that can be divided by each of the numbers from 1 to 10 without any
	remainder.
</p>
<p>
	What is the smallest positive number that is <dfn title="divisible with no remainder"
		>evenly divisible</dfn
	> by all of the numbers from 1 to 20?
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
