<script>
  import { url } from '@roxi/routify';
  import IconifyIcon from '@iconify/svelte'
  import bugIcon from '@iconify-icons/mdi/shield-bug'
</script>

<a href={$url('./index')} class="logoContainer">
  <IconifyIcon icon={bugIcon} color={'#01a954'} width={35} />
  <h1>Bed Bug Eliminators</h1>
</a>

<style>

  .logoContainer {
    display: flex;
    align-items: center;
    cursor: pointer;
    text-decoration: none;
    color: white;
    margin-left: 20px;
  }

  h1 {
    margin-left: 8px;
  }
</style>