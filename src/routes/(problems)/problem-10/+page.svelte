<script>
	function isPrime(n) {
		if (n < 2) {
			return false;
		}
		for (let i = 2; i <= Math.sqrt(n); i++) {
			if (n % i === 0) {
				return false;
			}
		}
		return true;
	}
	// given a natural number 'n', determine
	// if the number is prime or not
	let primes = [];
	function countPrimes() {
		for (let i = 2; i <= 2000000; i++) {
			if (isPrime(i)) {
				primes.push(i);
			}
		}

		return primes;
	}
	function sum(numbers) {
		return numbers.reduce((a, b) => a + b, 0);
	}

	let answer = sum(countPrimes());
</script>

<h1>Problem 10</h1>

<p>The sum of the primes below 10 is 2 + 3 + 5 + 7 = 17.</p>
<p>Find the sum of all the primes below two million.</p>

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
