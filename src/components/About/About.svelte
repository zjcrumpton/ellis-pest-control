<script>
  import { fly } from 'svelte/transition'
</script>


<section in:fly={{x: 500, duration: 500, delay: 500 }} out:fly={{x: -500, duration: 500 }}>
  <h1 class="left">About Bed Bug Eliminators</h1>

  <div class="about">
    <h2 class="left">Who We Are</h2>
    <p>
      Bed Bug Eliminators is family owned and operated. After 9 years of experience serving the Denver population as employees, we decided to open up our own company. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </p>
  </div>

  <div class="what">
    <h2 class="right">What We Do</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
  </div>

  <div class="who">
    <h2 class="left">Where We Serve</h2>
    <p>
      Denver, Colorado. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
  </div>

</section>

<style>
  section {
    font-family: Roboto;
    margin-top: 100px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }

  h1 {
    color: white;
    font-size: 2.5em;
    font-weight: 900;
    margin: 20px 0;
    text-align: left;
    margin-left: 40px;
  }

  h2 {
    color: #01a954;
    font-size: 1.8em;
    font-weight: 900;
    margin: 20px 0;
    margin-bottom: 30px;
  }

  p {
    color: #d7d8db;
    font-size: 1em;
    max-width: 900px;
    margin-right: 40px;
  }




  div {
    margin-bottom: 40px;
    margin-left: 40px;
  }


</style>