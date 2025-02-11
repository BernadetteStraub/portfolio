<script>
    import { onMount } from "svelte";

    export let text = ""; // The text to type
    export let speed = 100; // Typing speed in milliseconds per character
    let typedText = ""; // The visible text
    let index = 0;
  
    function type() {
      if (index < text.length) {
        typedText += text[index];
        index++;
        setTimeout(type, speed);
      }
    }
  
    // Start typing when the component is mounted
    onMount(() => {
      type();
    });
  </script>
  
  <div>
    <span>{typedText}</span><span class="cursor"></span>
  </div>

  <style>
    .cursor {
      display: inline-block;
      width: 1rem;
      height: 2rem;
      background-color: currentColor;
      margin-left: 0.4rem;
      vertical-align: -0.2rem;
      animation: blink 0.7s steps(1) infinite;
    }
  
    @keyframes blink {
      50% {
        background-color: transparent;
      }
    }
  </style>