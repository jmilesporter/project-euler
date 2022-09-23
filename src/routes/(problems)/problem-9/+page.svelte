<script>
	function pythagoreanTriplet() {
		for (let a = 1; a < 1000; a++) {
			for (let b = 1; b < 1000; b++) {
				for (let c = 1; c < 1000; c++) {
					if (a + b + c === 1000 && a < b && b < c && a * a + b * b === c * c) {
						return a * b * c;
					}
				}
			}
		}
	}

	let answer = pythagoreanTriplet();
</script>

<h1>Problem 9</h1>

<p>
	A Pythagorean triplet is a set of three natural numbers, <var>a</var> &lt; <var>b</var> &lt;
	<var>c</var>, for which,
</p>
<p>
	<var>a</var><sup>2</sup> + <var>b</var><sup>2</sup> = <var>c</var><sup>2</sup>
</p>
<p>For example, 3<sup>2</sup> + 4<sup>2</sup> = 9 + 16 = 25 = 5<sup>2</sup>.</p>
<p>
	There exists exactly one Pythagorean triplet for which <var>a</var> + <var>b</var> + <var>c</var>
	= 1000.<br />Find the product <var>abc</var>.
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
