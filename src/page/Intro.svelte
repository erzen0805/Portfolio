<script>
  let stylish=$$props.style;
</script>

<main class="container" style={stylish}>
  <div class="vertical-center">
    <div style="text-align: center;">
      <div class="title">D<span class="o">O</span>NG HYUN</div>
      <div class="subtitle">PORTFOLIO</div>
    </div>
  </div>
  <div class="no-print floating-letters1" style="left: 10vw; top: 5vh; animation-delay: 0.5s;">
    D
  </div>
  <div class="no-print floating-letters2" style="left: 30vw; top: 15vh; ">
    O
  </div>
  <div class="no-print floating-letters1" style="left: 57vw; top: 12vh;">
    N
  </div>
  <div class="no-print floating-letters2" style="left: 80vw; top: 17vh; animation-delay: 0.5s;">
    G
  </div>
  <div class="no-print floating-letters1" style="left: 16vw; top: 40vh;">
    H
  </div>
  <div class="no-print floating-letters2" style="left: 12vw; top: 70vh;">
    Y
  </div>
  <div class="no-print floating-letters1" style="left: 45vw; top: 80vh; animation-delay: 0.5s;">
    U
  </div>
  <div class="no-print floating-letters2" style="left: 72vw; top: 72vh;">
    N
  </div>
  <div class="no-print floating-letters1" style="left: 85vw; top: 50vh;">
    ♡
  </div>
</main>

<style>
.container {
  height: 100vh;
  position: relative;
  /* border: 3px solid green; */
  font-family: KoHo;
  user-select: none;
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
.floating-letters1 {
  position: absolute;
  font-size: 5vw;
  font-weight: 900;
  animation: 1s ease 0s infinite alternate none running movement;
  color: #313131; 
}
.floating-letters2 {
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
