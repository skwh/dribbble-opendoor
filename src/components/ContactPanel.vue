<template>
  <div class="contact-panel">
    <div class="contact-details">
      <div class="profile-photo">
      </div>
      <p class="name">
        Amy Cuo
      </p>
      <p class="email">
        <a href="#">
          contact@opendoor.com
        </a>
      </p>
      <p class="phone">
        555-555-5555
      </p>
    </div>
    <div class="contact">
      <p>Need help?</p>
      <button>
        Email
      </button>
      <button>
        SMS
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OpendoorContactPanel'
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

.contact-panel {
  grid-row-start: 3;
  grid-column-start: 6;

  .contact-details, .contact {
    text-align: center;
    color: $grey;
    a {
      color: $blue;
    }
  }

  .contact-details {
    font-size: 0.85rem;

    p {
      margin: 0.5rem 0rem;

      &:first-of-type {
        margin-top: 0.75rem;
      }
    }

    .profile-photo {
      display: block;
      height: 75px;
      width: 75px;
      border-radius: 100%;
      background-color: #ccc;
      margin: auto;
    }
  }

  .contact {
    p {
      font-size: 1.15rem;
      font-weight: 500;
      margin-bottom: 0.25rem;
    }
    button {
      border: 1px solid $button-border;
      border-radius: 5px;
      background-color: transparent;
      padding: 1rem 2rem;
      color: $grey;
      margin: 0.5rem;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.25s;

      &:hover {
        background-color: $button-border;
      }
    }
  }
}
</style>
