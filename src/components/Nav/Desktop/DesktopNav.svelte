<script>
  import {isActive, url} from '@roxi/routify';
  import Logo from '../Logo/Logo.svelte';
  import Button from '../../ui/Button/Button.svelte';
  import Hamburger from '../Hamburger/Hamburger.svelte'

  // Props
  export let toggleOpen;
  export let links;


</script>

<nav>
  <Logo />

  <!-- Only shows on desktop  -->
  <div class="navMenu">
    {#each links as [path, name]}
      <li >
        <a href={$url(path)}  class:active={$isActive(path)}>
          {name}
        </a>
      </li>
    {/each}
  </div>

  <Button type='navLink' text='Build a Quote' link='./booking' />

  <!-- Only shows on mobile -->
  <Hamburger action={toggleOpen} />
</nav>


<style>
  .active { color: #17ad64; }

  a {
    text-decoration: none;
    color: #fff;
    display: flex;
    align-items: center;
    text-decoration: none;
    padding: 0 1rem;
    height: 100%;
    cursor: pointer;
  }

  .navMenu {
    display: flex;
    align-items: center;
    margin-right: 50px;
    margin-right: 30px;
  }

  a:hover {
    transition: all 0.2s ease-in-out;
    color: #17ad64;
  }

  li {
    text-decoration: none;
    list-style-type: none;
  }

  nav {
    background: #000000;
    height: 50px;
    display: flex;
    justify-content: space-between;
    padding: 8px;
    z-index: 10;
    font-family: Roboto, sans-serif;
    font-size: 1.2em;
    color: white;
  }

  @media screen and (max-width: 860px) {
    .navMenu {
      display: none;
    }
  }
</style>