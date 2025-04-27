---
layout: default
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

<link rel="stylesheet" href="/portafolio_grupo_D_uc/Richard-Nina Chicaña/assets/css/custom.css">


<header class="profile-header">
  <div class="profile-text">
    <h1>👨‍💻 Richard Ángel Nina Chicaña Coloma</h1>
    <p class="subtitle">Docente y Especialista en Redes, Ciberseguridad y Educación Tecnológica</p>
    <div class="contact-info">
      <p><i class="fas fa-map-marker-alt"></i> Arequipa, Perú</p>
      <p><i class="fas fa-envelope"></i> jNina Chicañac@tecsup.edu.pe</p>
      <p><i class="fas fa-globe"></i> <a href="https://www.linkedin.com/in/Richard-ac28/" target="_blank">LinkedIn</a></p>
    </div>
  </div>
  <img src="/portafolio_grupo_D_uc/Richard-Nina Chicaña/assets/images/logo.jpg" alt="Richard Ángel Nina Chicaña" class="profile-img">
</header>

---

## 🧠 Sobre Mí

Soy un profesional apasionado por las **tecnologías de la información y la educación**, con experiencia en la implementación de **redes inalámbricas**, **seguridad informática**, **virtualización** y **sistemas operativos Linux**. Actualmente me desempeño como **docente** en TECSUP, donde diseño experiencias de aprendizaje significativas en carreras técnicas.

---

## 💼 Experiencia Profesional

{% for job in site.data.experience %}
<div class="experience-card">
  <h3>{{ job.position }}</h3>
  <div class="job-meta">
    <span class="company"><strong>{{ job.company }}</strong></span>
    <span class="duration">📅 {{ job.duration }}</span>
    {% if job.location %}<span class="location">📍 {{ job.location }}</span>{% endif %}
  </div>
  
  <div class="job-description">
    {{ job.description | markdownify }}
  </div>
  
  {% if job.responsibilities %}
  <div class="responsibilities">
    <h4>Funciones destacadas:</h4>
    <ul>
      {% for item in job.responsibilities %}
      <li>{{ item }}</li>
      {% endfor %}
    </ul>
  </div>
  {% endif %}
  
  {% if job.technologies %}
  <div class="technologies">
    <h4>Tecnologías utilizadas:</h4>
    <div class="tech-tags">
      {% for tech in job.technologies %}
      <span class="tech-tag">{{ tech }}</span>
      {% endfor %}
    </div>
  </div>
  {% endif %}
</div>
{% endfor %}

---

## 🧩 Habilidades Técnicas

{% for category in site.data.skills.categories %}
<div class="skills-category">
  <h3>{{ category.name }}</h3>
  <div class="skills-list">
    {% for skill in category.skills %}
    <div class="skill-item">
      <span class="skill-name">{{ skill.name }}</span>
      <div class="skill-level">
        <div class="skill-bar" style="width: {{ skill.level }}%"></div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
{% endfor %}

---

## 🎓 Formación Académica

{% for education in site.data.education %}
<div class="education-card">
  <h3>{{ education.degree }}</h3>
  <div class="education-meta">
    <span class="institution">{{ education.institution }}</span>
    <span class="year">📅 {{ education.year }}</span>
  </div>
  {% if education.description %}
  <p>{{ education.description }}</p>
  {% endif %}
</div>
{% endfor %}

---

## 🛠 Proyectos Destacados

<div class="projects-grid">
  {% for project in site.data.projects %}
  <div class="project-card">
    <h3>{{ project.name }}</h3>
    <div class="project-meta">
      <span class="year">📅 {{ project.year }}</span>
      {% if project.client %}<span class="client">👨‍💼 {{ project.client }}</span>{% endif %}
    </div>
    <p>{{ project.description }}</p>
    <div class="project-tech">
      {% for tech in project.technologies %}
      <span class="tech-tag">{{ tech }}</span>
      {% endfor %}
    </div>
    {% if project.link %}
    <a href="{{ project.link }}" target="_blank" class="project-link">Ver detalles</a>
    {% endif %}
  </div>
  {% endfor %}
</div>

---

## 📢 Tecnologías y Herramientas

<div class="tools-section">
  {% for tool in site.data.tools %}
  <div class="tool-item">
    <img src="/assets/images/tools/{{ tool.icon }}" alt="{{ tool.name }}" class="tool-icon">
    <span class="tool-name">{{ tool.name }}</span>
  </div>
  {% endfor %}
</div>

---

## 📫 Contacto

<div class="contact-section">
  <div class="contact-form">
    <h3>Envíame un mensaje</h3>
    <form action="https://formspree.io/f/your-form-id" method="POST">
      <input type="text" name="name" placeholder="TU NOMBRE" required>
      <input type="email" name="email" placeholder="TU COPRREO" required>
      <textarea name="message" placeholder="Tu mensaje" required></textarea>
      <button type="submit">Enviar</button>
    </form>
  </div>
  <div class="contact-details">
    <h3>Mis redes</h3>
    <div class="social-links">
      <a href="https://www.linkedin.com/in/Richard-ac28/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
      <a href="mailto:jNina Chicañac@tecsup.edu.pe"><i class="fas fa-envelope"></i> Email</a>
      <a href="#" target="_blank"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>
</div>



<script>
  // Scripts opcionales para funcionalidad adicional
  document.addEventListener('DOMContentLoaded', function() {
    // Puedes añadir interactividad aquí
  });
</script>
