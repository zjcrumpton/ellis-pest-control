<script>
  import IconifyIcon from '@iconify/svelte';
  import expand from '@iconify-icons/mdi/arrow-expand'
  import collapse from '@iconify-icons/mdi/arrow-collapse'


  // Props
  export let setActive;
  export let id;
  export let expanded;
  export let icon;
  export let title;       
  export let content = "Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Quisque ut sollicitudin libero. Proin sapien quam, lacinia nec ipsum vitae, maximus malesuada dui. Fusce nibh arcu, dignissim sed velit sit amet, dapibus suscipit massa. Sed porta nulla at rhoncus rhoncus. Maecenas sagittis eros in mauris ornare, ut mattis orci dignissim. Morbi et ultrices orci, vitae malesuada orci. Nulla in auctor ligula, sed tincidunt lectus. Pellentesque nec feugiat metus, condimentum volutpat turpis. Donec pulvinar elit id purus elementum, ut bibendum elit vulputate.";
</script>

<article on:click={()=>setActive(id)} class={!expanded ? "closed" : "open"} >
  <IconifyIcon {icon} color="#01a954" width={80} />
  <h2>{title}</h2>
  <p class={expanded ? 'showContent' : ""}>
    {content}
  </p>
  <div>
    <IconifyIcon icon={expanded ? collapse : expand} color="#01a954" width={30} />
  </div>

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
  div {
    margin-top: 15px;
  }

  p {
    display: none;
    overflow: hidden;
    color: #d7d8db;
    line-height: 1.5em;
    margin-top: 15px;
    margin-bottom: 10px;
    text-align: center;
    
  }
  .showContent{
    display: block;
  }
  .closed {
    max-height: 180px;
  }

  h2 {
    font-size: 1.5em;
    margin-top: 15px;
  }
</style>