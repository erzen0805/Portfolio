<script>
  let stylish=$$props.style;

  const alphabets = [
    { text: "D", position: "left: 10vw; top: 5%;" },
    { text: "O", position: "left: 30vw; top: 15%;" },
    { text: "N", position: "left: 57vw; top: 12%;" },
    { text: "G", position: "left: 80vw; top: 17%;" },
    { text: "H", position: "left: 16vw; top: 40%;" },
    { text: "Y", position: "left: 12vw; top: 70%;" },
    { text: "U", position: "left: 45vw; top: 80%;" },
    { text: "N", position: "left: 72vw; top: 72%;" },
    { text: "♡", position: "left: 85vw; top: 50%;" },
  ];
</script>

<main class="container" style={stylish}>
  <div class="vertical-center">
    <div style="text-align: center;">
      <div class="title">D<span class="o">O</span>NG HYUN</div>
      <div class="subtitle">PORTFOLIO</div>
    </div>
  </div>
  {#each alphabets as { text, position }, i}
  <div class="no-print floating-letters{i%2}" style="{position}; animation-delay: 0.{i}s;">
    {text}
  </div>
  {/each}
</main>

<style>
.container {
  height: 100vh;
  min-height: 400px;
  /* border: 3px solid green; */
  font-family: KoHo;
  user-select: none;
  position: relative;
}
@media (max-height: 400px) {
  .container {
    height: unset;
    min-height: 400px;
  }
}
.vertical-center {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.title {
  font-size: 9.3rem;
  font-family: 'Keania One', cursive;
  color: rgb(184, 232, 41);
}
.subtitle {
  font-size: 2rem;
  font-weight: 700;
  letter-spacing: 2px;
  color: white;
  font-family: KoHo;
}
.o {
  position: relative;
}
.o::before {
  left: 0px;
  content: "";
  display: block;
  position: absolute;
  width: 0px;
  height: 0px;
  border-bottom: 27px solid rgb(184, 232, 41);
  border-left: 15px solid transparent;
  border-right: 15px solid transparent;
  top: calc(50% - 0.33em);
  transform: translate(0px, -50%) rotate(-33.6deg);
}
.o::after {
  right: 0px;
  content: "";
  display: block;
  position: absolute;
  width: 0px;
  height: 0px;
  border-bottom: 27px solid rgb(184, 232, 41);
  border-left: 15px solid transparent;
  border-right: 15px solid transparent;
  top: calc(50% - 0.33em);
  transform: translate(0px, -50%) rotate(33.6deg);
}
.floating-letters0 {
  position: absolute;
  font-size: 5vw;
  font-weight: 900;
  animation: 1s ease 0s infinite alternate none running movement;
  color: #313131; 
}
.floating-letters1 {
  position: absolute;
  font-size: 5vw;
  font-weight: 900;
  animation: 1s ease 0s infinite alternate none running movement;
  color: #000000;
}
@keyframes movement {
  from {
    filter: brightness(60%);
    transform: scale(0.8) rotate(0deg);
  }
  to {
    filter: brightness(100%);
    transform: scale(1.2) rotate(360deg);
  }
}
</style>
