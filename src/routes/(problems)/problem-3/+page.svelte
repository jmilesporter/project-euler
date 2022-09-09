<script>
	function largestPrimeFactor(number) {
		let array = [];
		let primes = [];
		let multiple = 2;
		for (let i = 0; i < number; i++) {
			if (array.some((n) => n === multiple)) {
				multiple++;
			} else {
				for (let j = multiple; j < number; j += multiple) {
					if (j === multiple) {
						primes.push(j);
					} else {
						array.push(j);
					}
				}
				multiple++;
			}
		}
		let primeFactors = [];
		primes.filter((n) => number % n === 0).forEach((n) => primeFactors.push(n));
		return Math.max(...primeFactors);
	}

	let answer = largestPrimeFactor(99999);
	console.log(answer);
</script>

<h1>Problem 3</h1>
<p>The prime factors of 13195 are 5, 7, 13 and 29.</p>
<p>What is the largest prime factor of the number 600851475143 ?</p>

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
