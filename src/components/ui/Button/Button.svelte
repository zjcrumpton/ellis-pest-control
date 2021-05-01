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
    border: 3px solid #01a954;
    outline: none;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    text-decoration: none;
    font-weight: bold;
    font-size: .9em;
  }

  a:link { text-decoration: none; }

  .m10 {
    display: flex;
    align-items: center;
    border-radius: 4px;
    background: #01a954;
    padding: 10px 22px;
    color: #fff;
    border: 3px solid #01a954;
    outline: none;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.2em;
    margin: 10px;
    height: 45px;
  }

  .m10-clear {
    display: flex;
    align-items: center;
    border-radius: 4px;
    background: none;
    padding: 10px 22px;
    color: #fff;
    border: 3px solid #01a954;
    outline: none;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.2em;
    margin: 10px;
    height: 45px;
  }

  .m10-clear:hover {
    transition: all 0.2s ease-in-out;
    background: #01a954;
    color: white;
  }

  div {
    display: flex;
    align-items: center;
  }

  button:hover {
    transition: all 0.2s ease-in-out;
    background: none;
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