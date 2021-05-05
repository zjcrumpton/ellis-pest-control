<script>
  import IconifyIcon from '@iconify/svelte';
  import book from '@iconify-icons/mdi/book-open-page-variant';
  import restore from '@iconify-icons/mdi/restore';
  import bug from '@iconify-icons/mdi/bug';
  import table from '@iconify-icons/mdi/table-furniture';
  import Graphic from './Graphic/Graphic.svelte'

  
  



</script>

<section id="info">
  <header>
    <h1>Our Process</h1>
    <hr>

    <h3>
      We're here to help at every step of the way.
    </h3>

  </header>
  <div>
    <Graphic 
      icon={book} 
      title="Educate" 
    />
   
    <Graphic 
      icon={table}
      title="Prep"
    />

    <Graphic 
      icon={bug}
      title="Exterminate"
    />

    <Graphic 
      icon={restore}
      title="Restore"
    />
  </div>
</section>

<style>
  section {
    margin-top: 100px;
    height: 20000px;
    font-family: Roboto, sans-serif;
    color: white;
    padding: 20px;
    padding-top: 50px;
  }

  h1 {
    display: flex;
    justify-content: center;
    font-size: 1.8em;
  }

  h3 {
    color: #d7d8db;
    text-align: center;
    margin-top: 40px;
  }

  div {
    display: flex;
    justify-content: space-between;
    margin: 40px;
    margin-top: 50px;
  }
  hr {
    width: 6em;
    height: 3px;
    background-color: #01a954;
    border: none;
    color: #01a954;
  }

  @media screen and (max-width: 1100px) {
    div {
      display: flex;
      justify-content: flex-start;
      flex-direction: column;
    }
  }
</style>