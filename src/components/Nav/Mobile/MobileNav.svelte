<script>
  import IconifyIcon from '@iconify/svelte';
  import closeMenu from '@iconify-icons/mdi/close-thick';
  import {isActive, url} from '@roxi/routify';
  import Button from '../../ui/Button/Button.svelte';

  export let toggleOpen;
  export let isOpen;
  export let links;

</script>

<aside class={`${isOpen ? 'visible' : 'hidden'}`}>
  <button on:click={toggleOpen} class={`${isOpen ? 'visible' : 'hidden'}`}>
    <IconifyIcon 
      icon={closeMenu} 
      color={'white'} 
      width={40} 
    />
  </button>

  <div>
    {#each links as [path, name]}
      <li >
        <a href={$url(path)} class:active={$isActive(path)} on:click={toggleOpen}>
          {name}
        </a>
      </li>
    {/each}

    <div class="flex-center">
      <Button action={toggleOpen} type='link' text='Build a Quote' link='./booking' />
    </div>
  </div>


</aside>

<style>
  .visible {
    display: block;
  }

  .hidden {
    display: none;
  }

  .active { color: #17ad64; }

  .flex-center {
    display: flex;
    justify-content: center;
  }

  aside {
    position: fixed;
    z-index: 10000;
    width: 100%;
    height: 100%;
    background: #161d25;
    display: grid;
    align-items: center;
    top: 0;
    left: 0;
    transition: 0.3s ease-in-out;
    top: 0;
    font-family: Robot, sans-serif;
    overflow: hidden;
  }

  button {
    background: none;
    border: none;
    cursor: pointer;
    position: absolute;
    top: 1.2rem;
    right: 1.5rem;
  }

  li {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    text-decoration: none;
    transition: 0.2s ease-in-out;
    color: #fff;
    cursor: pointer;
  }

  a {
    text-decoration: none;
    color: white;
  }

  a:hover {
    color: #01bf71;
    transition: 0.2s ease-in-out;
  }

  div {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: repeat(6, 60px);
    text-align: center;
    margin-top: 100px;
  }
</style>