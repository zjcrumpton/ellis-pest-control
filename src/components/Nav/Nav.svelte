<script>
  import MobileNav from './Mobile/MobileNav.svelte';
  import DesktopNav from './Desktop/DesktopNav.svelte';
  import IconifyIcon from '@iconify/svelte'
  import phoneIcon from '@iconify-icons/mdi/phone-classic'



  let isOpen = false;
  const links = [
    ['./index', 'Home'],
    ['./education', 'Education'],
    ['./about-us', 'About Us'],
    ['./contact', 'Contact'],
  ]

  const toggleOpen = () => {
    isOpen = !isOpen;
  }
</script>

<MobileNav {links} {isOpen} {toggleOpen} />
<DesktopNav {links} toggleOpen={toggleOpen}/>
<div class="phone">
  <IconifyIcon icon={phoneIcon} color="#d7d8db" />
  <a href="tel:7208282847">
    <span>720-828-BUGS (2847)</span>
  </a>
</div>

<style>
  .phone {
    position: absolute;
    top: 90px;
    right: 50px;
    font-family: Roboto, sans-serif;
    color: #d7d8db;
    font-size: 1.5em;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  span { 
    margin-left: 10px;
  }

  a {
    text-decoration: none;
    color: #d7d8db;
  }
</style>