<script>
  import IconifyIcon from '@iconify/svelte'
  import phone from '@iconify-icons/mdi/phone'
  import email from '@iconify-icons/mdi/email'
  import cal from '@iconify-icons/mdi/calendar-edit'
  import fb from '@iconify-icons/mdi/facebook'
  import tw from '@iconify-icons/mdi/twitter'
  import ig from '@iconify-icons/mdi/instagram'




</script>

<div class="contactLinks">
  <div class="top">
    <h1>Get in touch</h1>
    <p>Fill out the form and our team will get back to you shortly. If you're ready to book an appointment, please click "Build a Quote" below.</p>
  </div>
  
  <div class="links">
    <div class="link">
      <IconifyIcon  icon={phone} color="#01a954" width={30} />
      <a href="tel:7208282847">
        <h2>720-828-BUGS (2847)</h2>
      </a>
    </div>

    <div class="link">
      <IconifyIcon  icon={email} color="#01a954" width={30} />
      <a href="mailto:info@bbe-bedbugeliminators.com">
        <h2>info@bbe-bedbugeliminators.com</h2>
      </a>
    </div>

    <div class="link">
      <IconifyIcon  icon={cal} color="#01a954" width={30} />
      <a href="/booking">
        <h2>Build a Quote and Book an Appointment</h2>
      </a>
    </div>
  </div>

  <div class="socialLinks">
    <div class="sc">
      <IconifyIcon icon={fb} color="#d7d8db" width={50} />
    </div>
    <div class="sc">
      <IconifyIcon icon={tw} color="#d7d8db" width={50} />
    </div>
    <div class="sc">
      <IconifyIcon icon={ig} color="#d7d8db" width={50} />
    </div>
  </div>
</div>

<style>
  div {
    font-family: Roboto;
    color: white;
    max-width: 600px;
  }

  .contactLinks {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-left: 40px;
    margin-bottom: 40px;
  }

  .socialLinks {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px;
    margin-top: 40px;
  }

  .sc {
    margin-right: 50px;
    cursor: pointer;
  }

  .top {
    margin-top: 100px;
    line-height: 35px;
  }

  h1 {
    font-size: 2.5em;
    font-weight: 900;
    margin: 20px;
  }

  p {
    color: #d7d8db;
    margin: 20px;
    font-size: 1.5em;
    margin-bottom: 40px;
    margin-top: 30px;
  }

  .link {
    display: flex;
    align-items: center;
    font-size: 20px;
    margin: 20px;
    cursor: pointer;
  }

  .link h2 {
    margin-left: 20px;
    color: #d7d8db;
  }

  a {
    text-decoration: none;
  }

  @media screen and (max-width: 1000px) {
    .contactLinks {
      margin: 0;
    }

    .link {
      margin-bottom: 10px;
      margin-top: 10px;
    }

    p {
      margin-bottom: 20px;
      margin-top: 15px;
    }

    h1 {
      margin-bottom: 10px;
      margin-top: 10px;
    }

    .socialLinks {
      margin: 10px;
      margin-bottom: 40px;
    }
    .top {
      margin-top: 80px;
    }
  }
</style>