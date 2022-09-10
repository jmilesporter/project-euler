<script>
	function largestPalindrome(a, b) {
		let product = a * b;
		let firstHalf = [];
		let secondHalf = [];
		function isPalindrome(n) {
			let number = n.toString().split('');

			for (let i = 0; i < Math.floor(number.length / 2); i++) {
				firstHalf.push(number[i]);
			}
			if (number.length % 2 === 0) {
				for (let i = Math.floor(number.length / 2); i < number.length; i++) {
					secondHalf.push(number[i]);
				}
			} else {
				for (let i = Math.floor(number.length / 2) + 1; i < number.length; i++) {
					secondHalf.push(number[i]);
				}
			}
		}
		isPalindrome(product);
		let first = parseInt(firstHalf.join(''));
		let second = parseInt(secondHalf.reverse().join(''));
		if (first === second) {
			return true;
		} else {
			return false;
		}
	}
	let palindromes = [];

	for (let k = 1000; k > 0; k--) {
		for (let l = 1000; l > 0; l--) {
			let candidate = largestPalindrome(k, l);
			if (candidate === true) {
				palindromes.push(k * l);
			}
		}
	}

	let answer = Math.max(...palindromes);
	console.log(answer);
</script>

<h1>Problem 4</h1>

<p>
	A palindromic number reads the same both ways. The largest palindrome made from the product of two
	2-digit numbers is 9009 = 91 × 99.
</p>
<p>Find the largest palindrome made from the product of two 3-digit numbers.</p>

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
