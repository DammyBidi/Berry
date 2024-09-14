<template>
  <div class="home">
    <MobileNav />
    <div class="hero-section">
      
      <div class="hero-content">
        <h1>Explore our endless thrills</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur. Arcu ornare ipsum metus
          elementum est euismod pulvinar.Lorem ipsum dolor sit amet consectetur.
          Arcu ornare ipsum metus elementum est euismod pulvinar.
        </p>
        <button>See Our Services</button>
        <div class="hero-image">
          <img src="../assets/images/Neon futuristic VR.svg" alt="" />
        </div>
      </div>
      <div class="nav">
        <div class="logo">
          <img src="../assets/images/Logo.svg" alt="logo" />
          <p>Berry</p>
        </div>
        <div class="home">
          <img src="../assets/images/HouseLine.svg" alt="house-logo" />
          <p>Home</p>
        </div>
        <div class="about">
          <router-link to="/about"><img src="../assets/images/UsersThree.svg" alt="" /></router-link>
          <!-- <img src="../assets/images/UsersThree.svg" alt="" /> -->
        </div>
      </div>
    </div>

    <!--First Section -->

    <div class="first-section">
      <div class="text">
        <div class="first">
          <h2>Why Choose us?</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur. Arcu ornare ipsum metus
            elementum est euismod pulvinar.
          </p>
        </div>
        <div class="second">
          <div>
            <button>Perfect Sitting Area</button>
            <button>Cool Gadgets</button>
            <button>Super Power Computers</button>
          </div>
          <div>
            <button class="blue">Gaming Pad</button>
            <button>Super Power Computers</button>
          </div>
        </div>

        <div class="mobile-second" ref="mobileSecondContainer">
          <button>Super Power Computers</button>
          <button class="blue">Gaming Pad</button>
          <button>Super Power Computers</button>
          <button>Perfect Sitting Area</button>
          <button>Cool Gadgets</button>
        </div>
      </div>

      <div class="image-container" ref="firstImageContainer">
        <img src="../assets/images/choose1.svg" alt="" />
        <img src="../assets/images/choose2.svg" alt="" />
        <img src="../assets/images/choose3.svg" alt="" />
        <img src="../assets/images/choose4.svg" alt="" />
        <img src="../assets/images/choose5.svg" alt="" />
      </div>
    </div>

    <!--Second Section -->

    <div class="second-section" >
      <div class="text">
        <h1>
          Experience the lorem ipsum <br />
          the lorem ipsun
        </h1>
        <div>
          <button class="blue">Single Play</button>
          <button>Team Play</button>
        </div>
      </div>

      <div class="image-container" ref="secondImageContainer">
        <img src="../assets/images/experience1.svg" alt="" />
        <img src="../assets/images/experience2.svg" alt="" />
        <img src="../assets/images/experience3.svg" alt="" />
        <img src="../assets/images/experience4.svg" alt="" />
        <img src="../assets/images/experience5.svg" alt="" />
      </div>
    </div>

    <!--Third Section -->
    <div class="third-section">
      <h1>Everything You Need For The Perfect Gaming Experience</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur. Arcu ornare ipsum metus
        elementum est euismod pulvinar.
      </p>
    </div>

    <!--Fourth Section -->

    <div class="fourth-section">
      <div class="card-container">
        <div class="left">
          <div class="card">
            <img src="../assets/images/GamepadIcon.svg" alt="GamepadIcon" />
            <h3>Immersive Story Gameplay</h3>
            <p>
              Our games offer immersive gameplay experiences that transport
              players to captivating worlds filled with adventure, challenges,
              and excitement.
            </p>
          </div>
          <div class="card">
            <img src="../assets/images/GamepadIcon.svg" alt="GamepadIcon" />
            <h3>Community and Engagement</h3>
            <p>
              Join a vibrant community of gamers who share your passion for
              gaming. Participate in forums, share tips and strategies, and stay
              up-to-date on the latest news and updates from the studio.
            </p>
          </div>
        </div>
        <div class="right">
          <div class="card">
            <img src="../assets/images/GamepadIcon.svg" alt="GamepadIcon" />
            <h3>Diverse Selection of Titles</h3>
            <p>
              Whether you're into action-packed adventures, strategic
              simulations, or immersive role-playing games, you'll find a game
              that speaks to your interests and preferences.
            </p>
          </div>
        </div>
      </div>
      <div class="image">
        <img src="../assets/images/VRimage.svg" alt="VRimage" />
      </div>
      <div class="mobile-image">
        <img src="../assets/images/Mobile-VRimage.svg" alt="" />
      </div>
    </div>

    <!-- Footer -->
    <footer>
      <div class="text">
        <h1>Get in touch</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur. Arcu ornare ipsum metus
          elementum est euismod pulvinar.
        </p>
      </div>
      <div class="social-links">
        <div>
          <img src="../assets/images/whatsApp-logo.svg" alt="whatsapp-logo" />
          <p>+123 456 7890</p>
        </div>
        <div>
          <img src="../assets/images/facebook-logo.svg" alt="facebook-logo" />
          <p>@blueberry</p>
        </div>
        <div>
          <img src="../assets/images/instagram-logo.svg" alt="instagram-logo" />
          <p>blue_berry</p>
        </div>
        <div>
          <img src="../assets/images/instagram-logo.svg" alt="twitter-fill" />
          <p>@bluetwitter</p>
        </div>
      </div>
      <div>
        <hr />
        <div class="footer-bottom">
          <div>
            <img src="../assets/images/Logo.svg" alt="logo" />
            <h1>Berry</h1>
          </div>
          <p>©copyright 2024</p>
          <div>
            <p>Home</p>
            <p>Services</p>
            <p>Contact</p>
          </div>
        </div>
        <div class="mobile-footer-bottom">
          <div>
            <img src="../assets/images/Logo.svg" alt="logo" />
            <h1>Berry</h1>
          </div>
          <div class="footer-bottom-link">
            <div>
              <p>Home</p>
              <p>Services</p>
              <p>Contact</p>
            </div>
            <p>©copyright 2024</p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import MobileNav from '@/components/MobileNav.vue';

// References for the image containers
const firstImageContainer = ref<HTMLElement | null>(null);
const secondImageContainer = ref<HTMLElement | null>(null);
  const mobileSecondContainer = ref<HTMLElement | null>(null);

const startContinuousScrolling = (container: HTMLElement, direction: 'left' | 'right' = 'left') => {
  const scrollSpeed = 1; 

  
  const content = container.innerHTML;
  container.innerHTML += content;

  const scroll = () => {
    if (direction === 'left') {
      container.scrollLeft += scrollSpeed;
      if (container.scrollLeft >= container.scrollWidth / 2) {
        container.scrollLeft = 0;
      }
    } else {
      container.scrollLeft -= scrollSpeed;
      if (container.scrollLeft <= 0) {
        container.scrollLeft = container.scrollWidth / 2;
      }
    }

    requestAnimationFrame(scroll);
  };

  scroll();
};

onMounted(() => {
  if (firstImageContainer.value) {
    startContinuousScrolling(firstImageContainer.value, 'left');
  } 

  if (secondImageContainer.value) {
    startContinuousScrolling(secondImageContainer.value, 'right');
  } 

  if (mobileSecondContainer.value) {
    startContinuousScrolling(mobileSecondContainer.value, 'right');
  }
});
</script>

<style scoped>
@import "../assets/styles/home.css";
</style>
