<script>
	import { onDestroy } from 'svelte';
	let endDate = new Date('01/01/2023 00:00:00');

	let seconds = 0;
	let minutes = 0;
	let hours = 0;
	let days = 0;

	// tick sets time calculation for days, hours, minutes, secs
	function tick() {
		let remaining_seconds = Math.floor((endDate - new Date()) / 1000);

		seconds = Math.floor(remaining_seconds % 60);
		minutes = Math.floor((remaining_seconds % 3600) / 60);
		hours = Math.floor((remaining_seconds % (3600 * 24)) / 3600);
		days = Math.floor(remaining_seconds / (3600 * 24));
	}
	tick();
	let intervalId = setInterval(tick, 1000);

	onDestroy(() => clearInterval(intervalId));
</script>

<section class="release">
	<h2>We Will Release OSF Academy</h2>
	<p>We are working hard and estimated release time products below.</p>
	<p>Sed ac trisque nunc, ut gravida nunc. Nulla consequat erat non lectus imperdiet.</p>
	<div class="counterdown container container-fluid">
		<div on:click={tick} class="row justify-content-center">
			<div class="col">
				<div class="days counter ">{days}</div>
				<div class="counter-text">Days</div>
			</div>
			<div class="col">
				<div class="hours counter ">{hours}</div>
				<div class="counter-text ">Hours</div>
			</div>
			<div class="col">
				<div class="minutes counter ">{minutes}</div>
				<div class="counter-text ">Minutes</div>
			</div>
			<div class="col">
				<div class="seconds counter ">{seconds}</div>
				<div class="counter-text">Seconds</div>
			</div>
		</div>
	</div>

	<div class=" container-input container-fluid">
		<input
			type="email"
			name="email"
			placeholder="Enter your email to receive the latest annoucements"
			required
		/>
		<button type="submit"> <i class="bi bi-caret-right-fill" /> </button>
	</div>
</section>

<style>
	.release {
		background-color: #fff;
		display: block;
		margin-top: 70px;
		margin-bottom: 70px;
		margin-left: 63px;
		width: 90%;
		height: 600px;
	}
	.release h2 {
		text-align: center;
		font-weight: 500;
		font-family: 'Times New Roman', Times, serif;
		padding-top: 60px;
	}
	.release p {
		text-align: center;
		font-family: 'Times New Roman', Times, serif;
		margin-bottom: 2px;
	}
	.counterdown {
		width: fit-content;
		padding-top: 90px;
		padding-bottom: 70px;
	}

	.counter{
		width: 160px;
		border-radius: 50%;
		font-size: 60px;
		padding: 10px 25px;
		text-align: center;
		font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
		background: -webkit-linear-gradient(#eee, #333);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	
	.counter-text {
		text-align: center;
		font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
		font-size: 24px;
		color: rgb(44, 43, 43);
	}
	input[name='email'] {
		width: 500px;
		border-radius: 14px;
		border: 1px solid rgb(104, 122, 89);
		text-align: left;
		padding: 5px 10px;
	}
	.container-input {
		text-align: center;
		padding-bottom: 60px;
		position: relative;
		width: fit-content;
	}
	.container-input button[type='submit'] {
		color: #a3cd59;
		background-color: inherit;
		position: absolute;
		top: 3px;
		right: 16px;
		border: 1px solid #a3cd59;
		border-radius: 50%;
		padding: 2px 5px;
	}
</style>
