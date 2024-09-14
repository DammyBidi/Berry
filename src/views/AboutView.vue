<template>
  <div class="about">
    <mobile-nav />
    <div class="hero-section">
      
      <div class="hero-content">
        <h1>ABOUT US</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur. Arcu ornare ipsum metus
          elementum est euismod pulvinar.Lorem ipsum dolor sit amet consectetur.
          Arcu ornare ipsum metus elementum est euismod pulvinar.
        </p>
      </div>
      <div class="nav">
        <div class="logo">
          <img src="../assets/images/Logo.svg" alt="logo" />
          <p>Berry</p>
        </div>
        <div class="home">
          <router-link to="/"
            ><img src="../assets/images/HouseLine.svg" alt="house-logo"
          /></router-link>
          <p>Home</p>
        </div>
        <div class="about">
          <router-link to="/about"
            ><img src="../assets/images/UsersThree.svg" alt=""
          /></router-link>
          <!-- <img src="../assets/images/UsersThree.svg" alt="" /> -->
        </div>
      </div>
    </div>

    <!-- Our mission -->
    <div class="mission">
      <div class="mission-text">
        <h2>Our Mission</h2>
        <p>
          BlueBerry Studios crafts immersive worlds, igniting imaginations &
          sparking adventures through innovative gameplay. We connect players &
          leave a lasting legacy
        </p>
      </div>
      <div class="mission-image">
        <img src="../assets/images/missionimage.svg" alt="" />
      </div>
    </div>

    <!-- Our Values -->

    <div class="our-value">
      <h2>Our Values</h2>
      <div class="values">
        <div class="value-section1">
          <div class="value-card">
            <img src="../assets/images/Star.svg" alt="" />
            <h3>Creativity</h3>
            <p>
              We believe in fostering a culture of creativity and innovation,
              where bold ideas are celebrated and imagination knows no bounds.
            </p>
          </div>
          <div class="value-card">
            <img src="../assets/images/Star.svg" alt="" />
            <h3>Excellence</h3>
            <p>
              We are committed to excellence in everything we do, striving to
              deliver the highest quality games, experiences, and services to
              our players.
            </p>
          </div>
          <div class="value-card">
            <img src="../assets/images/Star.svg" alt="" />
            <h3>Community</h3>
            <p>
              We are dedicated to building inclusive, supportive communities
              where players can connect, collaborate, and thrive.
            </p>
          </div>
        </div>
        <div class="value-section2">
          <div class="value-card">
            <img src="../assets/images/Star.svg" alt="" />
            <h3>Passion</h3>
            <p>
              Passion is at the heart of everything we create. We are driven by
              a deep love for gaming and a desire to share that passion with
              players around the world.
            </p>
          </div>
          <div class="value-card">
            <img src="../assets/images/Star.svg" alt="" />
            <h3>Integrity</h3>
            <p>
              Integrity is non-negotiable. We uphold the highest ethical
              standards in our business practices, treating our players,
              partners, and team members with honesty, respect, and fairness
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Our Team -->
    <div class="our-team">
      <div class="team-text">
        <h2>Meet Our Team</h2>
        <p>
          Meet the incredible team at BlueBerry Studios that helps to shape the
          future of gaming and leave a lasting impact on the world.
        </p>
      </div>
      <div class="image-container" ref="firstImageContainer">
        <img src="../assets/images/Profile1.svg" alt="" />
        <img src="../assets/images/Profile2.svg" alt="" />
        <img src="../assets/images/Profile3.svg" alt="" />
        <img src="../assets/images/Profile4.svg" alt="" />
        <img src="../assets/images/Profile5.svg" alt="" />
      </div>
      <div class="image-container" ref="secondImageContainer">
        <img src="../assets/images/Profile6.svg" alt="" />
        <img src="../assets/images/Profile7.svg" alt="" />
        <img src="../assets/images/Profile8.svg" alt="" />
        <img src="../assets/images/Profile9.svg" alt="" />
        <img src="../assets/images/Profile10.svg" alt="" />
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
import { ref, onMounted } from "vue";
import MobileNav from "@/components/MobileNav.vue";

const firstImageContainer = ref<HTMLElement | null>(null);
const secondImageContainer = ref<HTMLElement | null>(null);

const startContinuousScrolling = (
  container: HTMLElement,
  direction: "left" | "right" = "left"
) => {
  const scrollSpeed = 1;

  const content = container.innerHTML;
  container.innerHTML += content;

  const scroll = () => {
    if (direction === "left") {
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
  if (firstImageContainer.value && secondImageContainer.value) {
    startContinuousScrolling(firstImageContainer.value);
    startContinuousScrolling(secondImageContainer.value, "right");
  }
});
</script>

<style scoped>
@import "../assets/styles/about.css";
</style>
