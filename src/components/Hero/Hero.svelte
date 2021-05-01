<script>
  import IconifyIcon from '@iconify/svelte'
  import bugIcon from '@iconify-icons/mdi/shield-bug-outline'
  import downIcon from '@iconify-icons/mdi/arrow-down-thick'
  import phoneIcon from '@iconify-icons/mdi/phone-classic'
  import Button from '../ui/Button/Button.svelte'
</script>

<section>
  <div class="phone">
    <IconifyIcon icon={phoneIcon} color="#d7d8db" />
    <h2>1-800-214-8911</h2>
  </div>
  <div class="content">
    <div class="textContent">
      <h1>Nobody Likes Bed Bugs</h1>
      <p>
        <span>We get rid of them.</span> 
        Our heat treatment services are effective, affordable, and backed by a guarantee.
      </p>

      <ul>
        <li>Locally Owned</li>
        <li>Safe & Chemical-Free</li>
        <li>All We Do Is Bed Bugs</li>
      </ul>

      <div class="buttons">
        <Button text="Build a Quote" type="m10"/>
        <Button text="Learn More" type="m10-clear"/>
      </div>

    </div>
    <div class="homeImage">
      <IconifyIcon 
        icon={bugIcon} 
        width="100%"
        color="#01a954"
        />
    </div>
  </div>

  <div class="flex-center">
    <IconifyIcon icon={downIcon} width="5%"  />
  </div>
</section>

<style>
  .flex-center {
    display: flex;
    justify-content: center;
    margin-top: 40px;
    cursor: pointer;
    color: white;
  }

  .flex-center:hover {
    transition: all 0.2s ease-in-out;
    color: #17ad64;
  }

  section {
    padding: 50px;
    padding-top: 100px;
  }

  .content {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-template-rows: 1;
    font-family: Roboto, sans-serif;
  }

  .textContent {
    grid-column: 1/2;
    width: 100%;
    height: auto;
    margin-left: 20%;
  }

  span {
    color: #1fc776;
  }

  .homeImage {
    width: 60%;
    height: auto;
    grid-column: 2/3;
    margin-left: 30%;
  }

  .buttons {
    display: flex;
    align-items: center;
    margin-top: 20px;
  }

  h1 {
    color: white;
    font-size: 4.2vw;
    line-height: 1;
    margin: 0 auto;
    font-weight: 900;
  }

  ul {
    margin-top: 15px;
    color: #d7d8db;
    font-size: 1.9vw;
  }

  li {
    margin-bottom: 10px;
    list-style: none;
  }
  li::before {content: "•"; color:#01a954; margin-right: 10px; }

  p {
    margin-top: 30px;
    color: #d7d8db;
    font-size: 2vw;
    line-height: 1.3;
  }

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

  h2 { 
    margin-left: 10px;
  }
</style>