<template>  
  <div class="contact">
      <form id="contact-form" @submit.prevent="sendEmail">        
        <h2>Name</h2>
        <input type="text" name="user_name" id="user_name"><br />
        <h2>Email</h2>
        <input type="email" name="user_email" id="user_email"><br />
        <h2>Message</h2>
        <textarea name="message" id="message"></textarea><br />
        <input type="submit" value="Send" id="contactbtn">
    </form>
  </div>
</template>
<script>
import emailjs from 'emailjs-com';
export default {
  name: "Contact",
  methods: {
    sendEmail: (e) => {
      emailjs.sendForm('gmail', 'servicerequest', e.target, 'user_mndCDpXc5cL8StwGUscg2')
        .then((result) => {
            e.target.reset();
        }, (error) => {
            alert("Failed to send message!");
            e.target.reset();
        });
    }
  }
}
</script>

