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
	function countPrimes() {
		let primes = [];
		for (let i = 2; i <= 1000000; i++) {
			if (isPrime(i)) {
				primes.push(i);
			}
		}

		return primes[10000];
	}
	let answer = countPrimes();
</script>

<h1>Problem 7</h1>

<p>
	By listing the first six prime numbers: 2, 3, 5, 7, 11, and 13, we can see that the 6th prime is
	13.
</p>
<p>What is the 10001st prime number?</p>

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
