<script>
  import IconifyIcon from '@iconify/svelte';
  import expand from '@iconify-icons/mdi/arrow-expand'
  import collapse from '@iconify-icons/mdi/arrow-collapse'


  // Props
  export let icon;
  export let title;       
  export let content = "Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Quisque ut sollicitudin libero. Proin sapien quam, lacinia nec ipsum vitae, maximus malesuada dui. Fusce nibh arcu, dignissim sed velit sit amet, dapibus suscipit massa. Sed porta nulla at rhoncus rhoncus. Maecenas sagittis eros in mauris ornare, ut mattis orci dignissim. Morbi et ultrices orci, vitae malesuada orci. Nulla in auctor ligula, sed tincidunt lectus. Pellentesque nec feugiat metus, condimentum volutpat turpis. Donec pulvinar elit id purus elementum, ut bibendum elit vulputate.";

  let open = false;
  const toggle = () => {
    open = !open;
  }
</script>

<article on:click={toggle} class={!open ? "closed" : "open"} >
  <IconifyIcon {icon} color="#01a954" width={80} />
  <h2>{title}</h2>

  {#if open}
    <p>
      {content}
    </p>

    <div>
      <IconifyIcon icon={collapse} color="#01a954" width={30} />
    </div>
  {:else}
    <div>
      <IconifyIcon icon={expand} color="#01a954" width={30} />
    </div>
  {/if}

</article>

<style>
  article {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    margin: 10px;
    border: 3px solid #01a954;
    padding: 20px;
    min-width: 180px;
    cursor: pointer;
  }

  article:hover {
    opacity: 70%;
  }

  div {
    margin-top: 15px;
  }

  p {
    color: #d7d8db;
    margin-top: 15px;
    margin-bottom: 10px;
    text-align: center;
  }

  .closed {
    max-height: 180px;
  }

  .open:hover {
    opacity: 100%;
  }

  h2 {
    font-size: 1.5em;
    margin-top: 15px;
  }
</style>