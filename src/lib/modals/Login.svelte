<script>
	import Modal from "$lib/modals/Modal.svelte";

	let showPassword=false;
	function toggle() {
		showPassword=!showPassword;
	}
</script>


<Modal on:close>
	<form>
		<h3>Sign in</h3>

		<label for="email">Email</label>
		<input type="email" name="email" required />

		<div class="forgot">
			<label for="password">Password</label>
			<a href="#">forgot password</a>
		</div>
		<div class="password">
			<i class="bi bi-eye" on:click={toggle }  />
			<!-- daca show_password e true, atunci type="text" daca e false, atunci type="password" -->
			<!-- hint: ternary operator in {} -->
			<input type="{showPassword?'text':'password'}" name="password"  pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{'{6,}'}" title="Password must contain at least 6 characters length, contain 1 numeric, 1 uppercase letter, 1 special character" minlength="6" required />
		</div>

		<input type="submit" value="Login" class="login" />
		<a href="#" class="register">I don't have an account</a>
	</form>

</Modal>

<style>
	form {
		width: 429px;
		height: 465px;
		text-align: center;
		border-radius: 10px;
		padding: 50px;
		background-color: white;
	}
	h3 {
		margin-top: 50px;
		font-weight: bold;
	}
	input[name='email'] {
		width: 300px;
		border-radius: 14px;
		border: 1px solid lightgray;
	}
	input[name='password'] {
		width: 300px;
		border-radius: 14px;
		border: 1px solid lightgray;
	}
	input[type='submit'].login {
		display: block;
		margin: 60px auto 25px;
		border-color: transparent;
		color: #ffffff;
		background-color: #84bc22;
		padding: 8px 20px;
		border-width: 2px;
		border-style: solid;
		border-radius: 35px;
		cursor: pointer;
		text-transform: uppercase;
		font-size: 18px;
		padding: 9px 80px;
	}
	input[type='submit'].login:hover {
		color: #84bc22;
		border-color: #84bc22;
		background-color: #ffffff;
	}
	.forgot a {
		text-decoration: none;
		color: #84bc22;
		font-size: 16px;
	}
	.register {
		text-decoration: none;
		color: #84bc22;
		font-size: 16px;
	}
	label[for='email'] {
		width: 100%;
		margin-left: 10px;
		padding-right: 250px;
		margin-top: 30px;
	}
	label[for='password'] {
		margin-left: 10px;
		padding-right: 100px;
		margin-top: 20px;
	}
	.password {
		position: relative;
	}
	.password i {
		position: absolute;
		right: 20px;
		top: 3px;
	}
</style>
