<script>
  import IconifyIcon from '@iconify/svelte';
  import menuIcon from '@iconify-icons/mdi/menu';

  export let action = () => {
    console.log('Hamburger Menu was pressed')
  };
</script>

<div on:click={action}>
  <IconifyIcon icon={menuIcon} class='hamburger' width={40} height={40} />
</div>

<style>
  div {
    display: flex;
    align-items: center;
    margin-right: 30px;
    cursor: pointer;
  }

  @media screen and (min-width: 861px) {
    div {
      display: none;
    }
  }
</style>