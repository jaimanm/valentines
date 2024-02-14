<script>
  let button = document.getElementById("button");
  // @ts-ignore
  // get the x and y position fo the button
  let x, y;
  let index = 0;

  function handleButtonClick() {
    // move the button to a random position within the visible area
    x = Math.random() * (window.innerWidth - button.offsetWidth);
    y = Math.random() * (window.innerHeight - button.offsetHeight);
    if (index < texts.length - 1) {
      index++;
    }
  }

  let texts = [
    "No :(",
    "Nope.",
    "Sorry, no.",
    "Not today.",
    "Never...",
    "No way!",
    "Please stop",
    "I said no!",
    "No means no!",
    "No, no, no!",
    "Stop clicking me!",
    "I'm serious!",
    "I'm not kidding!",
    "STOP CLICKING NO!",
    "i give up.",
  ];
</script>

<button
  bind:this={button}
  id="button"
  class="btn bg-red-300 px-4 py-2 absolute mx-5"
  style="top: {y}px; left: {x}px;"
  on:click={handleButtonClick}
>
  {texts[index]}
</button>
