<div class="header">
	<nav class="nav">
		<ul>
			<li>
				<span>Lifecycle методи</span>

				<ul>
					<li>
						<a href="/lifecycle-methods/on-mount">onMount()</a>
					</li>
					<li>
						<a href="/lifecycle-methods/on-destroy">onDestroy()</a>
					</li>
				</ul>
			</li>

			<li>
				<span>Bind</span>

				<ul>
					<li>
						<a href="/bind/value">bind:value</a>
					</li>
					<li>
						<a href="/bind/checked">bind:checked</a>
					</li>

					<li>
						<a href="/bind/this">bind:this</a>
					</li>
				</ul>
			</li>

			<li>
				<span>Runes</span>

				<ul>
					<li>
						<a href="/runes/state">&#36;state</a>
					</li>

					<li>
						<a href="/runes/derived">&#36;derived</a>
					</li>

					<li>
						<a href="/runes/effect">&#36;effect</a>
					</li>

					<li>
						<a href="/runes/props">&#36;props</a>
					</li>
				</ul>
			</li>

			<li>
				<span>Специални елементи</span>

				<ul>
					<li>
						<a href="/special-elements/svelte-head">&#60;svelte:head&#62;</a>
					</li>

					<li>
						<a href="/special-elements/svelte-document">&#60;svelte:document&#62;</a>
					</li>
				</ul>
			</li>
		</ul>
	</nav><!-- /.nav -->
</div><!-- /.header -->

<style>
	.nav ul {
		list-style-type: none;
	}

	.nav > ul {
		display: flex;
	}

	.nav > ul > li {
		flex-grow: 1;
		text-align: center;
		background: rgb(46, 50, 59);
		position: relative;
	}

	.nav > ul > li:nth-child(even) {
		background: rgb(22, 25, 31);
	}

	.nav > ul > li a,
	.nav > ul > li > span {
		display: block;
		color: #fff;
		text-decoration: none;
		font-weight: 500;
		font-size: 20px;
		transition: color .4s;
	}

	.nav > ul > li > a,
	.nav > ul > li > span {
		padding: 20px 10px;
	}

	@media(hover: hover) and (pointer: fine) {
		.nav > ul > li a:hover,
		.nav > ul > li > span:hover {
			cursor: pointer;
			color: rgb(165, 207, 39);	
		}
	}

	.nav > ul > li ul {
		position: absolute;
		top: 100%;
		left: 0;
		width: 100%;
		text-align: center;
		background: rgb(22, 25, 31);
		padding: 10px 0;
		opacity: 0;
		visibility: hidden;
		transition: opacity .4s, visibility .4s;
	}

	.nav > ul > li:hover ul {
		opacity: 1;
		visibility: visible;
	}

	.nav > ul > li ul a {
		padding: 10px;
	}
</style>