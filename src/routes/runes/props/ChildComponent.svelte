<script>
	let props = $props();
</script>

<div class="section">
	<div class="container section__container">
		<div class="section__box">
			<h2>
				This component is <span>{props.adjective}</span>!
			</h2>
		</div><!-- /.section__box -->
	</div><!-- /.container -->
</div><!-- /.section -->

<style>
	/* Section */
	.section {
		padding: 100px 0;
		display: flex;
		flex-grow: 1;
	}

	.section .section__container {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.section .section__box {
		width: 100%;
		background: rgb(231, 231, 231);
		padding: 40px;
		border-radius: 20px;
		color: rgb(46, 50, 59);
		text-align: center;
		min-height: 300px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.section .section__box > *:not(:last-child) {
		margin-bottom: 30px;
	}

	.section .section__box h2 span {
		color: rgb(165, 207, 39);
	}
</style>