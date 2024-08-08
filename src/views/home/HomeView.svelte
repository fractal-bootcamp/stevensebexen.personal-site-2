<script lang='ts'>
    import Title from './Title.svelte';
</script>

<div id='view-home'>
  <Title on:changeview />
  <p id='name'>Steven Sebexen</p>
  <div id='next'>This is the point at which words fail to convey the meaning to which they were assigned.</div>
</div>

<style>
  #view-home {
    display: flex;
    position: relative;
    flex: 1 1 0px;
  }

  #name {
    cursor: default;
    position: absolute;
    left: 17%;
    top: 35%;
    transform: rotate(-12deg);
    font-size: 8rem;
    letter-spacing: 12px;
    color: black;
    font-family: "Teko";
    animation: sway 6s ease-in-out 0s infinite alternate;
  }

  #next {
    cursor: default;
    position: absolute;
    color: white;
    font-family: "Space Grotesk";
    font-size: 2rem;
    width: 30%;
    right: 6%;
    bottom: 3%;
    pointer-events: none;
  }

  @keyframes sway {
    from {transform: rotate(-14deg);}
    to {transform: rotate(-11deg);}
  }
</style>