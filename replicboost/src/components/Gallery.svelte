<script>
  let slides = [
    { src: "static/joey-banks-YApiWyp0lqo-unsplash.jpg" },
    { src: "static/olav-tvedt-yq-efMJMuPg-unsplash.jpg" },
    { src: "static/patrick-tomasso-CP1cKFIl7qc-unsplash.jpg" }
  ];
  let cur = 0;
  function changeSlied(slide) {
    cur = slide;
  }
  const clamp = (number, min, max) => Math.min(Math.max(number, min), max);
  const transitionArgs = {
    duration: 200
  };
  function prev(e) {
    cur = clamp(--cur, 0, slides.length - 1);
  }
  function next(e) {
    cur = clamp(++cur, 0, slides.length - 1);
  }
  const ARROW_LEFT = 37;
  const ARROW_RIGHT = 39;
  function handleShortcut(e) {
    if (e.keyCode === ARROW_LEFT) {
      prev();
    }
    if (e.keyCode === ARROW_RIGHT) {
      next();
    }
  }
</script>

<style>
  button {
    background: transparent;
    color: #fff;
    border-color: transparent;
    width: 3.2rem;
    height: 3.2rem;
  }
  button:hover,
  button:focus {
    background: rgba(0, 0, 0, 0.5);
  }
  .extra-outer-wrapper {
    display: inline-block;
    width: 100%;
    position: relative;
    margin: auto;
    z-index: 33;
  }

  .outer-wrapper {
    width: 100%;
    padding: 0 0 650px;
    position: relative;
  }

  .inner-wrapper {
    min-height: 100%;
    width: 100%;
    position: absolute;
  }

  .prev,
  .next {
    cursor: pointer;
    position: absolute;
    top: 48%;
    width: auto;
    margin-top: -22px;
    padding: 16px;
    color: white;
    font-weight: bold;
    font-size: 18px;
    transition: 0.6s ease;
    border-radius: 0 3px 3px 0;
    user-select: none;
  }
  .next {
    right: 0;
    border-radius: 3px 0 0 3px;
  }
  .slide {
   width: 100%;
   height: auto;
   max-height: 650px;
  }
</style>

<svelte:window on:keyup={handleShortcut} />
<div class="extra-outer-wrapper">
  <div class="outer-wrapper">
    <div class="inner-wrapper">
      {#each slides as slide, id}
        {#if id === cur}
          <div>
            <img class="slide" src={slide.src} alt="" />
          </div>
        {/if}
      {/each}
      <button class="prev" on:click={() => prev()}>&lt;</button>
      <button class="next" on:click={() => next()}>&gt;</button>
    </div>
  </div>
</div>
