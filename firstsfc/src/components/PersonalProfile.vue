<template>
  <header>
    <div class="header-content">
      <h1>Harvey</h1>
      <nav>
        <a href="#about">About</a>
        <a href="#gallery">Gallery</a>
        <a href="#">Resources</a> 
        <button @click="toggleDarkMode" id="themeBtn">Toggle Dark Mode</button>
      </nav>
    </div>
  </header>

  <main>
    <section id="about" class="hero-section">
      <div class="hero-container">
        <!-- Profile Image Placeholder (remove or replace when available) -->
        <div class="hero-image">
          <div class="placeholder">Profile Image</div>
        </div>
        <div class="hero-text">
          <h2>Hello, I'm <span class="highlight">Harvey</span></h2>
          <p>
            I’m an IT student passionate about web development, UI/UX design, and
            modern JavaScript frameworks like Vue.js. I focus on building clean,
            intuitive, and visually compelling websites while refining my skills.
          </p>
          <div class="hero-cards">
            <div class="card">
              <h3>Education</h3>
              <p>Currently pursuing a degree in IT, strengthening my foundation in programming, databases, and web technologies.</p>
            </div>
            <div class="card">
              <h3>Goals</h3>
              <p>Aspiring to create meaningful, accessible, and visually appealing web applications.</p>
            </div>
            <div class="card">
              <h3>Interests</h3>
              <p>UI/UX design, coding personal projects, learning frameworks, and improving user experiences.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="gallery">
      <h2>Portfolio</h2>
      <div class="gallery-grid">
        <!-- Placeholder for Gallery Images -->
        <div class="gallery-item">Image 1</div>
        <div class="gallery-item">Image 2</div>
        <div class="gallery-item">Image 3</div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Harvey | Portfolio</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      darkMode: false,
    };
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      document.body.classList.toggle('dark', this.darkMode);
    },
  },
};
</script>

<style scoped>
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: 'Helvetica', sans-serif;
  background: #fdfdfd;
  color: #1c1c1c;
  line-height: 1.6;
  transition: background 0.3s, color 0.3s;
}
h1,h2,h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; }
a { text-decoration: none; }

header {
  background: #000;
  color: #fff;
  padding: 15px 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
}
header .header-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  max-width: 100%;
}
header h1 {
  color: #dc143c;
  font-size: 3rem;
  font-weight: 900;
}
header nav {
  display: flex;
  align-items: center;
  gap: 16px;
}

header nav button {
  padding: 12px 24px;
  font-size: 1.2rem;
  font-weight: 700;
  background: #dc143c;
  border: none;
  border-radius: 8px;
  color: #fff;
  cursor: pointer;
  transition: background 0.3s, transform 0.2s;
}
header nav button:hover {
  background: #a90f2e;
  transform: scale(1.05);
}

header nav a { color: #fff; font-weight: 600; transition: color 0.3s; }
header nav a:hover { color: #dc143c; }

.hero-section { width: 100%; background: #f8f8f8; padding: 60px 20px; }
.hero-container { display: flex; flex-wrap: wrap; max-width: 100%; margin: auto; gap: 40px; align-items: center; justify-content: space-between; }
.hero-image .placeholder {
  width: 320px; height: 320px;
  background-color: #dc143c;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  font-size: 1.5rem;
}
.hero-text { flex: 1; min-width: 300px; }
.hero-text h2 { font-size: 2rem; margin-bottom: 16px; }
.hero-text .highlight { color: #dc143c; }
.hero-text p { font-size: 1.1rem; margin-bottom: 30px; color: #333; }

.hero-cards { display: flex; flex-wrap: wrap; gap: 20px; }
.card {
  background: #fff;
  padding: 25px;
  flex: 1 1 300px;
  border-radius: 12px;
  box-shadow: 0 6px 25px rgba(0,0,0,0.12);
  transition: transform 0.3s, box-shadow 0.3s;
  position: relative;
}
.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(220,20,60,0.3);
}
.card:hover h3 { text-decoration: underline; }
.card h3 { margin-bottom: 12px; color: #dc143c; font-size: 1.2rem; }

#gallery { padding: 60px 20px; }
#gallery h2 { text-align: center; margin-bottom: 40px; color: #dc143c; font-size: 2rem; }
.gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; }
.gallery-item { 
  width: 100%; 
  height: 360px;
  background-color: #e0e0e0; 
  display: flex;
  justify-content: center;
  align-items: center;
  color: #333;
  font-size: 1.2rem;
  border-radius: 12px;
}

footer { text-align: center; padding: 30px 20px; background: #000; color: #fff; font-size: 0.9rem; }

.dark { background: #121212; color: #f5f5f5; }
.dark .hero-section { background: #1a1a1a; }
.dark .hero-text p { color: #e0e0e0; }
.dark .card { background: #242424; }
.dark header { background: #000; }
.dark nav a { color: #f5f5f5; }
.dark nav a:hover { color: #dc143c; }
.dark header nav button { background: #dc143c; }
.dark .gallery-item { background-color: #333; }
</style>
