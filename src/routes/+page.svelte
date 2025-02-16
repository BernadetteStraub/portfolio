<script>
	import About from '$lib/components/About.svelte';
	import Projects from '$lib/components/Projects.svelte';
	import Experience from '$lib/components/Experience.svelte';
	import TypingAnimation from '$lib/components/TypingAnimation.svelte';
</script>

<div class="bg-surface-100" data-theme="skeleton">
	<div class="flex min-h-screen items-center justify-center">
		<div class="flex flex-col lg:flex-row h-full w-full max-w-[110rem]">
			<aside class="w-full lg:w-2/5 lg:h-screen lg:sticky lg:top-0 p-8 flex flex-col items-center">
				<div class="flex flex-col items-center justify-center py-16 text-center">
					<img class="mb-12 h-80 w-80 rounded-full " src="/images/berni.png" alt="avatar" />
					<p class="m-4 text-xl text-secondary-400">Hi, my name is</p>
					<h1 class="mb-2 text-3xl text-error-400">
						<TypingAnimation text="> Bernadette Straub" speed={150} />
					</h1>
					<p class="m-4 text-xl text-secondary-400">Fullstack Engineer</p>
					<div class="flex justify-center gap-4 py-2">
						<a
							href="/images/CVBernadette11:10.pdf"
							target="_blank"
							rel="noopener noreferrer"
							class="variant-soft-secondary btn"><i class="icon-file-text-alt"></i>&nbsp;Resumé</a
						>
						<a
							href="mailto:str.bernadette@gmail.com?subject=Hello%20Bernadette&body=I%20wanted%20to%20reach%20out%20to%20you..."
							class="variant-soft-secondary btn"><i class="icon-envelope-alt"></i>&nbsp;Contact</a
						>
					</div>
					<nav>
						<ul class="p-8">
							<li class="my-2 text-secondary-400 hover:text-error-400">
								<a class="text-xl no-underline transition-colors duration-200" href="#about"
									>About</a
								>
							</li>
							<li class="my-4 text-secondary-400 hover:text-error-400">
								<a class="text-xl no-underline transition-colors duration-200" href="#experience"
									>Experience</a
								>
							</li>
							<li class="my-4 text-secondary-400 hover:text-error-400">
								<a class="text-xl no-underline transition-colors duration-200" href="#projects"
									>Projects</a
								>
							</li>
						</ul>
					</nav>
					<div class="flex justify-center gap-4">
						<a
							class="text-secondary-400 hover:text-error-400"
							href="https://www.linkedin.com/in/bernadette-straub-b468a2220/"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="Linkedin Profile"><i class="icon-linkedin-sign icon-2x"></i></a
						>
						<a
							class="text-secondary-400 hover:text-error-400"
							href="https://github.com/BernadetteStraub"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="GitHub Profile"><i class="icon-github icon-2x"></i></a
						>
					</div>
				</div>
			</aside>
			<main class="w-full lg:w-3/5 p-8 overflow-auto">
				<section class="mb-8" id="about">
					<About></About>
				</section>
				<section class="mb-8" id="experience">
					<Experience></Experience>
				</section>
				<section class="mb-8" id="projects">
					<Projects></Projects>
				</section>
			</main>
		</div>
	</div>
</div>

<style>
	/* .sidebar {
		position: sticky;
		top: 0;
		align-self: start;
		height: 100vh;
		width: 40%;
		padding: 2rem;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
	} */

	/* GLOBAL */
	@font-face {
		font-family: 'JetBrainsMono';
		src: url('/fonts/ttf/JetBrainsMono-Bold.ttf') format('ttf');
	}

	:global(body) {
		font-family: 'JetBrainsMono', monospace;
	}
</style>
