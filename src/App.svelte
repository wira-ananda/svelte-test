<script>
  import palette from "./utils/palette";
  let darkMode = false;
  const paletteColor = palette.background;
</script>

<main
  style={darkMode
    ? `background: ${paletteColor.dark.primary}; color: ${paletteColor.light.primary}`
    : `background: ${paletteColor.light.secondary}; color: ${paletteColor.dark.secondary}`}
>
  <h1>{darkMode ? "🌙 Mode Gelap" : "☀️ Mode Terang"}</h1>
  <button
    style={!darkMode
      ? `background: ${paletteColor.dark.primary}; color: ${paletteColor.light.primary}`
      : `background: ${paletteColor.light.secondary}; color: ${paletteColor.dark.secondary}`}
    on:click={() => (darkMode = !darkMode)}
  >
    {darkMode ? "Ganti ke Terang" : "Ganti ke Gelap"}
  </button>
</main>

<style>
  main {
    text-align: center;
    padding: 2rem;
    width: 30vw;
    border-radius: 2rem;
    transition:
      background 0.3s,
      color 0.3s;
  }

  button {
    padding: 10px 20px;
    font-size: 1.2rem;
    cursor: pointer;
  }
</style>
