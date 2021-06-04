<script>
  import ContactLinks from './ContactLinks/ContactLinks.svelte'
  import Form from './Form/Form.svelte'
  import { fly } from 'svelte/transition'
</script>

<section class="contactContainer" in:fly={{x: 500, duration: 500, delay: 500 }} out:fly={{x: -500, duration: 500 }}>
  <ContactLinks />
  <Form />
</section>


<style>
  section {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
    width: 100%;
  }


  @media screen and (max-width: 1000px) {
    section {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }    
  }
</style>