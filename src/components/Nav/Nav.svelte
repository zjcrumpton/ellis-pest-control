<script>
  import MobileNav from './Mobile/MobileNav.svelte';
  import DesktopNav from './Desktop/DesktopNav.svelte';

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