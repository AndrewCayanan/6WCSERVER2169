<template>
  <div class="resume-container">
    <header class="header">
      <div class="name-title">
        <img class="profile-image" src="@/assets/profiles.jpg" alt="Andrew Cayanan" />
        
        <div class="name-info">
          <h1>Andrew Cayanan</h1>
          <p class="job-title">Web Developer</p>
        </div>
      </div>
      <div class="contact-info">
        <p>Email: <a href="mailto:cayanananandrew09@gmail.com">cayanananandrew09@gmail.com</a></p>
        <p>Phone: (+63) 977-013-5777</p>
      </div>
    </header>

    <section class="section profile-section">
      <h2>Profile</h2>
      <Profile />
    </section>

    <section class="section education-section">
      <h2>Education</h2>
      <Education />
    </section>

    <section class="section skills-section">
      <h2>Skills</h2>
      <Skills />
    </section>
  </div>
</template>

<script>
// Import components
import Profile from './components/Profile.vue'
import Education from './components/Education.vue'
import Skills from './components/Skills.vue'

export default {
  name: "App",
  components: { Profile, Education, Skills },
};
</script>

<style scoped>
/* Basic Styling for the Resume */
.resume-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  font-family: 'Arial', sans-serif;
  background-color: #f4f7fa;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Modify the color of the email link */
.header .contact-info a {
  color: #06402B; 
  text-decoration: none; 
}

.header .contact-info a:hover {
  color: #052f1b; 
  text-decoration: none;
}

.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 2rem;
}

.header .name-title {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
}

.profile-image {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  margin-right: 1rem;
}

.name-info h1 {
  margin: 0;
  font-size: 2.5rem;
  color: #333;
}

.name-info .job-title {
  font-size: 1.2rem;
  color: #555;
}

.header .contact-info p {
  margin: 0.5rem 0;
  font-size: 1rem;
  color: #555;
}

/* Section Styling */
.section {
  margin-bottom: 2rem;
  padding: 1.5rem;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-top: 3px solid #06402B;
}

.section h2 {
  font-size: 1.8rem;
  margin-bottom: 1.5rem;
  color: #333;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

ul li {
  font-size: 1rem;
  margin-bottom: 0.5rem;
  color: #555;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid #eee; /* Light dividing line between items */
}

ul li strong {
  font-weight: bold;
}

/* Profile Section */
.profile-section {
  background-color: #e7f3f3;
}

/* Education Section */
.education-section {
  background-color: #f7f7f7;
}

/* Skills Section */
.skills-section {
  background-color: #e7f3f3;
}

/* Media Queries for Responsiveness */

/* Tablet and Larger Devices */
@media (min-width: 768px) {
  .header {
    flex-direction: row;
    justify-content: space-between;
  }

  .header .name-title {
    flex: 2;
  }

  .header .contact-info {
    flex: 1;
    text-align: right;
  }

  .section h2 {
    font-size: 2rem;
  }
}

/* Mobile Devices */
@media (max-width: 767px) {
  .resume-container {
    padding: 1rem;
  }

  .header {
    flex-direction: column;
    text-align: center;
  }

  .header .name-title h1 {
    font-size: 2rem;
  }

  .header .name-title .job-title {
    font-size: 1rem;
  }

  .section h2 {
    font-size: 1.5rem;
  }

  .header .contact-info p {
    font-size: 1rem;
  }

  .section {
    margin-bottom: 1rem;
    padding: 1rem;
  }
}
</style>
