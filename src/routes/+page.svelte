<script>
	import About from '$lib/components/About.svelte';
	import Projects from '$lib/components/Projects.svelte';
	import Experience from '$lib/components/Experience.svelte';
	import TypingAnimation from '$lib/components/TypingAnimation.svelte';
	import Certificates from '$lib/components/Certificates.svelte';
</script>

<div class="bg-surface-100" data-theme="skeleton">
	<div class="flex min-h-screen items-center justify-center">
		<div class="flex flex-col lg:flex-row h-full w-full max-w-[90rem]">
			<aside class="w-full lg:w-2/5 lg:h-screen lg:sticky lg:top-0 p-6 flex flex-col items-center">
				<div class="flex flex-col items-center justify-center py-12 text-center">
					<img class="mb-7 h-64 w-64 rounded-full " src="/images/berni.png" alt="avatar" />
					<p class="m-2 text-lg text-secondary-400">Hi, my name is</p>
					<h1 class="mb-2 text-2xl text-error-400">
						<TypingAnimation text="> Bernadette Straub" speed={150} />
					</h1>
					<p class="m-2 text-lg text-secondary-400">Fullstack Engineer</p>
					<div class="flex justify-center gap-4 py-2">
						<a
							href="/images/BernadetteStraubCV1.pdf"
							target="_blank"
							rel="noopener noreferrer"
							class="variant-soft-secondary btn text-sm px-4 py-2"><i class="icon-file-text-alt"></i>&nbsp;Resumé</a
						>
						<a
							href="mailto:str.bernadette@gmail.com?subject=Hello%20Bernadette&body=I%20wanted%20to%20reach%20out%20to%20you..."
							class="variant-soft-secondary btn text-sm px-4 py-2"><i class="icon-envelope-alt"></i>&nbsp;Contact</a
						>
					</div>
					<nav>
						<ul class="p-6">
							<li class="my-2 text-secondary-400 hover:text-error-400">
								<a class="text-lg no-underline transition-colors duration-200" href="#about"
									>About</a
								>
							</li>
							<li class="my-3 text-secondary-400 hover:text-error-400">
								<a class="text-lg no-underline transition-colors duration-200" href="#experience"
									>Experience</a
								>
							</li>
							<li class="my-3 text-secondary-400 hover:text-error-400">
								<a class="text-lg no-underline transition-colors duration-200" href="#projects"
									>Projects</a
								>
							</li>
							<li class="my-3 text-secondary-400 hover:text-error-400">
								<a class="text-lg no-underline transition-colors duration-200" href="#certificates"
									>Certificates</a
								>
							</li>
						</ul>
					</nav>
					<div class="flex justify-center gap-3">
						<a
							class="text-secondary-400 hover:text-error-400"
							href="https://www.linkedin.com/in/bernadette-straub-b468a2220/"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="Linkedin Profile"><i class="icon-linkedin-sign icon-large"></i></a
						>
						<a
							class="text-secondary-400 hover:text-error-400"
							href="https://github.com/BernadetteStraub"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="GitHub Profile"><i class="icon-github icon-large"></i></a
						>
					</div>
				</div>
			</aside>
			<main class="w-full lg:w-3/5 p-6 overflow-auto">
				<section class="mb-6" id="about">
					<About></About>
				</section>
				<section class="mb-6" id="experience">
					<Experience></Experience>
				</section>
				<section class="mb-6" id="projects">
					<Projects></Projects>
				</section>
				<section class="mb-6" id="certificates">
					<Certificates></Certificates>
				</section>
			</main>
		</div>
	</div>
</div>

<style>

	/* GLOBAL */
	@font-face {
		font-family: 'JetBrainsMono';
		src: url('/fonts/ttf/JetBrainsMono-Bold.ttf') format('ttf');
	}

	:global(body) {
		font-family: 'JetBrainsMono', monospace;
	}
</style>
