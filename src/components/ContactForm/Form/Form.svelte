<script>
  import Button from '../../ui/Button/Button.svelte'
</script>


<div class="form">
  <form 
    class="fields" 
    method="POST" 
    action="https://formspree.io/f/xzbyrweb"
  >
    <h1>Contact Us</h1>

    <div>
      <h3>Your Name</h3>
      <input name="name">
    </div>
  
    <div>
      <h3>Email</h3>
      <input name="email_address">
    </div>
  
    <div>
      <h3>Phone Number (optional)</h3>
      <input name="phone_number">
    </div>
  
    <div>
      <h3>Message</h3>
      <textarea name="message"></textarea>
    </div>
    <div class="btn" type="submit">
      <Button text='Submit' />
    </div>
  </form>
</div>

<style>
  .form {
    width: 50%;
    height: 530px;
    max-width: 500px;
    margin-top: 100px;
    margin-right: 60px;
    margin-left: 40px;
    padding-right: 20px;
    border-radius: 4px;
    border: 3px solid #01a954;
    background-color: black;
    color: white;
    font-family: Roboto;
    display: flex;
    justify-content: center;
  }

  .fields {
    min-width: 80%;
  }
  textarea {
    width: 100%;
    height: 75px;
    background-color: #161d25;
    border: 3px solid #01a954;
    resize: none;
    margin-bottom: 20px;
    color: #d7d8db;
    padding: 10px;
  }

  input {
    width: 100%;
    border-radius: 4px;
    border: 3px solid #01a954;
    background-color: #161d25;
    margin-bottom: 20px;
    color: #d7d8db;
    padding-right: 10px;
    padding: 10px;
  }

  h1 {
    font-weight: 500;
    font-size: 30px;
    text-align: center;
    margin-top: 20px;
    margin-bottom: 10px;
  }

  h3 {
    margin-bottom: 10px;
  }

  .btn {
    margin: 0 auto;
  }

  @media screen and (max-width: 1000px) {
    .form {      
      max-width: 600px;
      min-width: 350px;
      margin: 0;
    }
  }
</style>