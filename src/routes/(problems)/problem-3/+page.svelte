<script>
	let number = 600851475143;
	let primes = [];
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
	function primesList(number) {
		for (let i = 2; i <= Math.sqrt(number); i++) {
			if (isPrime(i)) {
				primes.push(i);
			}
		}
	}
	primesList(number);
	let factors = [];
	function factorsList(number) {
		for (let i = 0; i < Math.sqrt(number); i++) {
			if (number % i === 0) {
				factors.push(i);
			}
		}
	}
	factorsList(number);

	function largestPrimeFactor(A, B) {
		let primeFactors = A.filter((n) => B.includes(n));
		if (primeFactors.length === 0) {
			return 'no prime factors';
		} else {
			return Math.max(...primeFactors);
		}
	}
	console.log(factors, primes);

	let answer = largestPrimeFactor(factors, primes);
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
