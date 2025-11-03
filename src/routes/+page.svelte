<script lang="ts">
	let title = "Welcome to Bag of Bread!";
</script>

<svelte:head>
	<title>Bag of Bread - Crumbs and Nuggets</title>
	<meta name="description" content="A collection of resources and information, baked to perfection" />
</svelte:head>

<div class="home">
	<div class="hero">
		<h1>{title}</h1>
		<p class="subtitle">Your go-to source for deliciously random crumbs of wisdom</p>
	</div>

	<div class="content-grid">
		<div class="card">
			<div class="card-icon">🥖</div>
			<h2>Fresh Content</h2>
			<p>Hot out of the oven and ready to consume</p>
		</div>

		<div class="card">
			<div class="card-icon">🥐</div>
			<h2>Flaky Resources</h2>
			<p>Layered with knowledge and buttery smooth</p>
		</div>

		<div class="card">
			<div class="card-icon">🥯</div>
			<h2>Well-Rounded Info</h2>
			<p>Everything you knead to know</p>
		</div>
	</div>
</div>

<style>
	.home {
		animation: fadeIn 0.5s ease-in;
	}

	@keyframes fadeIn {
		from {
			opacity: 0;
			transform: translateY(20px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.hero {
		text-align: center;
		padding: 3rem 1rem;
		background: rgba(255, 255, 255, 0.8);
		border-radius: 20px;
		margin-bottom: 3rem;
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
		border: 4px dashed #d2691e;
	}

	h1 {
		font-size: 3rem;
		color: #8b4513;
		margin: 0 0 1rem 0;
		text-shadow: 2px 2px 4px rgba(210, 105, 30, 0.3);
		transform: rotate(-1deg);
	}

	.subtitle {
		font-size: 1.3rem;
		color: #a0522d;
		margin: 0;
		font-style: italic;
	}

	.content-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
		gap: 2rem;
		padding: 1rem 0;
	}

	.card {
		background: rgba(255, 248, 220, 0.9);
		padding: 2rem;
		border-radius: 15px;
		text-align: center;
		transition: all 0.3s ease;
		border: 3px solid #daa520;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
	}

	.card:hover {
		transform: translateY(-8px) rotate(2deg);
		box-shadow: 0 12px 20px rgba(0, 0, 0, 0.2);
	}

	.card-icon {
		font-size: 4rem;
		margin-bottom: 1rem;
		filter: drop-shadow(2px 2px 4px rgba(0, 0, 0, 0.2));
	}

	.card h2 {
		color: #8b4513;
		margin: 0 0 1rem 0;
		font-size: 1.5rem;
	}

	.card p {
		color: #a0522d;
		margin: 0;
		line-height: 1.6;
	}

	@media (max-width: 768px) {
		h1 {
			font-size: 2rem;
		}

		.subtitle {
			font-size: 1.1rem;
		}

		.content-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
