<script>
export default {
  name: 'Footer',
  data() {
    return {
      socialMediaList: [
        {
          link: "#",
          iconClass: "fa-brands fa-square-facebook",
        },
        {
          link: "#",
          iconClass: "fa-brands fa-square-pinterest",
        },
        {
          link: "#",
          iconClass: "fa-brands fa-square-twitter",
        },
        {
          link: "#",
          iconClass: "fa-brands fa-linkedin",
        },
        {
          link: "#",
          iconClass: "fa-brands fa-square-instagram",
        },
      ],
      supportList: [
        'Contact Us',
        'Online Chat',
        'Whatsapp',
        'Telegram',
        'Snapchat',
      ],
      aboutList: [
        'About Us',
        'Blog',
        'Career',
        'Job',
        'In press',
      ],
      faqList: [
        'Account',
        'Order',
        'Delivery',
        'Payment',
        'Return'
      ],
      contactsList: [
        {
          link: '#',
          icon: 'fa-solid fa-location-arrow',
          info: '4500 Mercantile plaza,suite 300,fort wprth,TX,76137,USA'
        },
        {
          link: '#',
          icon: 'fa-solid fa-phone',
          info: '+1(817)901 3377'
        },
        {
          link: '#',
          icon: 'fa-solid fa-envelope',
          info: 'info@example.com'
        }
      ]
    }
  }
}
</script>


<template>

  <footer>
    
    <div class="top-footer">

      <div class="container">
        <div class="row">
  
          <div class="col">
            <h3>Get In Touch</h3>
            <span>Have a Question for us? We'll answer your problem here</span>
            <nav>
  
              <ul>
                <li v-for="(socialMedia, index) in socialMediaList" :key="index">
                  <a :href="socialMedia.link">
                    <i :class="socialMedia.iconClass"></i>
                  </a>
                </li>
              </ul>
  
            </nav>
          </div>
  
          <div class="col">
            <h3>Support</h3>
  
            <ul>
              <li v-for="(support, index) in supportList" :key="index">
                <a href="#">{{ support }}</a>
              </li>
            </ul>
  
          </div>
  
          <div class="col">
            <h3>About</h3>
  
            <ul>
              <li v-for="(about, index) in aboutList" :key="index">
                <a href="#">{{ about }}</a>
              </li>
            </ul>
  
          </div>
  
          <div class="col">
            <h3>Faq</h3>
  
            <ul>
              <li v-for="(faq, index) in faqList" :key="index">
                <a href="#">{{ faq }}</a>
              </li>
            </ul>
  
          </div>
  
          <div class="col contact-me">
            <h3>Contact Me</h3>
  
            <ul class="fa-ul">
              <li v-for="(contact, index) in contactsList" :key="index">
                  <a :href="contact.link">
                    <i :class="contact.icon" class="fa-li"></i>
                    <span>{{ contact.info }}</span>
                  </a>
                </li>
            </ul>
  
          </div>
  
        </div>
      </div>

    </div>

    <div class="bottom-footer">
      <h4>Copyright 2022 by AttdogMilo.com</h4>
    </div>
    
  </footer>

</template>


<style lang="scss" scoped>
@use '../scss/main.scss' as *;

footer {
  padding-top: 100px;
  // height: 400px;
  background-color: black;
  color: rgb(150, 150, 150);

  .top-footer {
    padding: 50px 0;
    border-bottom: 1px solid $grey;
  }

  .bottom-footer {
    h4 {
      padding: 30px;
      font-weight: 400;
      color: $whitesmoke;
      text-align: center;
    }
  }

  li {
    margin-bottom: 15px;
    a {
      color: rgb(150, 150, 150);
    }
  }


  h3 {
    color: $orange;
    margin-bottom: 30px;
  }

  .col {
    width: calc(100% / 5);
    padding: 0 20px;

    span {
      line-height: 24px;
    }
  }

  nav {
    display: flex;
    margin-top: 30px;
    align-items: center;

    li {
      display: inline-block;
      font-size: 1.4rem;
      margin-right: 10px;
    }
  }

  .contact-me {

    li {
      margin-bottom: 25px;
    }
    
    i {
      color: $orange;
    }
    .fa-ul {
      list-style-type: none;
      margin-left: var(--fa-li-margin,1.2em);
      padding-left: 0;
    }
  }
}
</style>