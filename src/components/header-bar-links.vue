<template>
  <div class="navbar-menu">
    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a :href="facebook" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-facebook fa-2x" aria-hidden="true"></i>
          </a>
          <a :href="insta" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-instagram fa-2x" aria-hidden="true"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      facebook: 'https://www.facebook.com/coloristfx/',
      insta: 'https://www.instagram.com/jessica_londrie/',
    };
  },
};
</script>
