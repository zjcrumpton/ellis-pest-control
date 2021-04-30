<script>
  export let text = '';
  export let type = 'default';
  export let link = './index';
  export let action = () => {
    console.log('button action clicked');
  }
</script>

{#if type === 'link' || type === 'navLink'}
  <div>
    <a href={link}>
      <button on:click={action} class={`default ${type === 'navLink' ? 'navLink' : ''}`}>
        {text}
      </button>
    </a>
  </div>
{:else}
  <button class={type}>
    {text}
  </button>
{/if}


<style>
  .default {
    display: flex;
    align-items: center;
    border-radius: 4px;
    background: #01a954;
    padding: 10px 22px;
    color: #fff;
    border: none;
    outline: none;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    text-decoration: none;
    font-weight: bold;
    font-size: .9em;
  }

  a:link { text-decoration: none; }

  div {
    display: flex;
    align-items: center;
  }

  button:hover {
    transition: all 0.2s ease-in-out;
    background: #57e87c;
    color: #010606;
  }

  .navLink {
    margin-right: 30px;
  }

  @media screen and (max-width: 860px) {
    .navLink {
      display: none; 
    }
  }
</style>