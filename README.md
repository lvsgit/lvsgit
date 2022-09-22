<style>
  @property --rotate {
    syntax: "<angle>";
    initial-value: 132deg;
    inherits: false;
  }
  body {
    margin: 0;
    padding: 0;
    background: black;
    background-size: cover;
  }
  #container {
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .card {
    position: relative;
    width: 90%;
    height: 80%;
    padding: 40px 0;
    text-align: center;
    background: #020117;
    border-radius: 6px;
  }
  .card::before {
    content: "";
    position: absolute;
    top: -5px;
    left: -5px;
    right: -5px;
    bottom: -5px;
    border-radius: 8px;
    background-image: linear-gradient(
      var(--rotate)
      , #ff2929, #ff5520, #ffdd00, #00dd45, #4500ff, #8a2be2, #ee60ee );
    z-index: -2;
    animation: spin 7s linear infinite;
  }
  .card::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: linear-gradient(
      var(--rotate)
      , #ff2929, #ff5520, #ffdd00, #00dd45, #4500ff, #8a2be2, #ee60ee );
    z-index: -1;
    filter: blur(60px);
    animation: spin 7s linear infinite;
  }
  @keyframes spin {
    0% {
      --rotate: 0deg;
    }
    10% {
      --rotate: 36deg;
    }
    20% {
      --rotate: 72deg;
    }
    30% {
      --rotate: 108deg;
    }
    40% {
      --rotate: 144deg;
    }
    50% {
      --rotate: 180deg;
    }
    60% {
      --rotate: 216deg;
    }
    70% {
      --rotate: 252deg;
    }
    80% {
      --rotate: 288deg;
    }
    90% {
      --rotate: 324deg;
    }
    100% {
      --rotate: 360deg;
    }
  }
</style>
<div id="container">
  <h1 class="card"><p style="color: red;font-size: 30px;">test</p></h1>
</div>
