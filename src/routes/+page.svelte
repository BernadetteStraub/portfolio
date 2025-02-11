<script>
    // import "./app.css";
    // import Navbar from "./components/Navbar.svelte";
    import About from "$lib/components/About.svelte";
    import Projects from "$lib/components/Projects.svelte";
    import Contact from "$lib/components/Contact.svelte";
    import Experience from "$lib/components/Experience.svelte";
    import Education from "$lib/components/Education.svelte";
    import TypingAnimation from "$lib/components/TypingAnimation.svelte";
    </script>
    
    <div class="bg-surface-100" data-theme="skeleton">
    <div class="main">
    <div class="container">
        <aside class="sidebar">
            <div class="sidebar-content">
                <img src="/images/berni.png" alt="avatar">
                <p class="text-secondary-400">Hi, my name is</p>
                <h1 class="text-error-400"><TypingAnimation text="> Bernadette Straub" speed={150} /></h1>
                <p class="text-secondary-400">Fullstack Engineer</p>
                <div class="flex justify-center gap-4 py-2">
                    <a
      href="/images/CVBernadette11:10.pdf"
      target="_blank"
      rel="noopener noreferrer"
      class="btn variant-soft-secondary"
    ><i class="icon-file-text-alt"></i>&nbsp;Resumé</a>
                    <a
                    href="mailto:str.bernadette@gmail.com?subject=Hello%20Bernadette&body=I%20wanted%20to%20reach%20out%20to%20you..."
                    class="btn variant-soft-secondary"
                  ><i class="icon-envelope-alt"></i>&nbsp;Contact</a>                
                </div>
                <nav>
                    <ul class="p-8">
                        <li class="text-secondary-400 hover:text-error-400 my-4"><a href="#about">About</a></li>
                        <li class="text-secondary-400 hover:text-error-400 my-4"><a href="#experience">Experience</a></li>
                        <li class="text-secondary-400 hover:text-error-400 my-4"><a href="#projects">Projects</a></li>
                        <!-- <li class="text-secondary-400 hover:text-error-400 my-4"><a href="#contact">Contact</a></li> -->
                    </ul>
                </nav>
                <div class="social-icons">
                    <a class="text-secondary-400 hover:text-error-400" href="https://www.linkedin.com/in/bernadette-straub-b468a2220/" aria-label="Linkedin Profile"><i class="icon-linkedin-sign icon-2x"></i></a>
                    <a class="text-secondary-400 hover:text-error-400" href="https://github.com/BernadetteStraub" aria-label="GitHub Profile"><i class="icon-github icon-2x"></i></a>
                </div>
            </div>
        </aside>
        <main>
            <section id="about">
                <About></About>
            </section>
            <section id="experience">
                <Experience></Experience>
            </section>
            <section id="projects">
                <Projects></Projects>
            </section>
        </main>
    </div>
</div>
<div class="text-error-400 flex justify-center"><p>Made with <i class="icon-heart"></i> by yours truly. Built with Svelte.</p></div>

</div>
    
    <style>
        /* .background {
            background: 
    radial-gradient(circle at 97% 2%, rgba(255, 130, 255, 0.95) 0%, transparent 15%),
    radial-gradient(circle at 90% 15%, rgba(255, 120, 90, 0.65) 0%, transparent 15%),
    
    radial-gradient(circle at 2% 97%, rgba(255, 130, 255, 0.95) 0%, transparent 15%),
    radial-gradient(circle at 15% 90%, rgba(255, 120, 90, 0.65) 0%, transparent 15%),
        floralwhite;
        } */

        .main {
        display: flex;
    justify-content: center; /* Center horizontally */
    align-items: center; /* Center vertically */
    min-height: 100vh; /* Ensure it takes the full viewport height */
        }

        .container {
            display: flex;
            height: 100%;
            max-width: 110rem;
        }
    
        img {
            width: 20rem;
            height: 20rem;
            border-radius: 50%;
            margin-bottom: 3rem;
            /* background-color: floralwhite;
            box-shadow: 10px 0px 50px rgba(255, 130, 255, 0.4), 
            -70px -70px 70px rgba(255, 120, 90, 0.3) */
        }
    
        .sidebar {
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
        }
    
        .sidebar-content {
            text-align: center;
            padding: 4rem 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    
        .sidebar h1 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }
    
        .sidebar p {
            font-size: 1.2rem;
            margin: 1rem;
        }
    
        nav ul li a {
            text-decoration: none;
            font-size: 1.2rem;
            transition: color 0.2s;
        }
    
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }
    
        main {
            width: 60%;
            padding: 2rem;
            overflow-y: hidden;
        }
    
        section {
            margin-bottom: 2rem;
        }

    
    /* GLOBAL */
    @font-face {
      font-family: 'JetBrainsMono';
      src: url('/fonts/ttf/JetBrainsMono-Bold.ttf') format('ttf');
    }
    
    :global(body) {
      font-family: 'JetBrainsMono', monospace;
    }
    </style>