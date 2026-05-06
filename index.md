---
layout: default
---

<!-- Hero Section -->
<section class="hero">
  <h1>perseverance.ai</h1>
  <p class="tagline">Building Intelligent Systems with AI & Agentic Patterns</p>
  <p class="description">
    Senior engineer with 13+ years of experience. Specialized in Big Data systems (Scala, Spark, Kafka). 
    Now exploring the exciting world of Agentic AI, LLMs, and building autonomous systems.
  </p>
</section>

<!-- About Me Section -->
<section id="about">
  <h2>About Me</h2>
  <div class="about-content">
    <p>
      I'm a passionate senior software engineer with over 13 years of experience building scalable systems. 
      My journey has taken me from full-stack web development (PHP, JavaScript) to mastering big data technologies 
      (Scala, Spark, Kafka, Microservices, ETLs).
    </p>
    <p>
      Recently, I developed a proof-of-concept system support bot using Agentic AI patterns, which sparked my deep interest in this space. 
      I'm now focused on exploring agentic AI, LLMs, and autonomous agents—building practical, production-ready systems 
      that showcase these emerging technologies.
    </p>
    <p>
      On this platform, I share my learnings, showcase real-world projects, and document my journey into AI/LLMs. 
      I believe in learning by doing, and I'm committed to building open-source projects that demonstrate 
      complex agentic AI patterns and best practices.
    </p>
  </div>
</section>

<!-- Skills Section -->
<section id="skills">
  <h2>Skills & Technologies</h2>
  <div class="skills-grid">
    <div class="skill-category">
      <h4>🤖 AI & Machine Learning</h4>
      <div class="skill-tags">
        <span class="skill-tag">Agentic AI</span>
        <span class="skill-tag">LLMs</span>
        <span class="skill-tag">Prompt Engineering</span>
        <span class="skill-tag">Agent Patterns</span>
        <span class="skill-tag">RAG</span>
      </div>
    </div>
    <div class="skill-category">
      <h4>🔥 Big Data & Stream Processing</h4>
      <div class="skill-tags">
        <span class="skill-tag">Scala</span>
        <span class="skill-tag">Apache Spark</span>
        <span class="skill-tag">Spark Streaming</span>
        <span class="skill-tag">Kafka</span>
        <span class="skill-tag">Python</span>
      </div>
    </div>
    <div class="skill-category">
      <h4>🏗️ Backend & Architecture</h4>
      <div class="skill-tags">
        <span class="skill-tag">Microservices</span>
        <span class="skill-tag">System Design</span>
        <span class="skill-tag">ETL/ELT</span>
        <span class="skill-tag">Distributed Systems</span>
        <span class="skill-tag">Database Design</span>
      </div>
    </div>
    <div class="skill-category">
      <h4>💻 Web Development</h4>
      <div class="skill-tags">
        <span class="skill-tag">PHP</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">API Design</span>
        <span class="skill-tag">REST</span>
        <span class="skill-tag">GraphQL</span>
      </div>
    </div>
    <div class="skill-category">
      <h4>🛠️ Tools & Platforms</h4>
      <div class="skill-tags">
        <span class="skill-tag">Docker</span>
        <span class="skill-tag">Kubernetes</span>
        <span class="skill-tag">Git</span>
        <span class="skill-tag">AWS</span>
        <span class="skill-tag">CI/CD</span>
      </div>
    </div>
  </div>
</section>

<!-- Featured Blog Posts -->
<section id="featured-posts">
  <h2>Latest Blog Posts</h2>
  <div class="featured-posts">
    {% for post in site.posts limit:3 %}
      <div class="post-card">
        <div class="post-date">{{ post.date | date: "%B %d, %Y" }}</div>
        <h3>{{ post.title }}</h3>
        <p class="post-excerpt">{{ post.excerpt }}</p>
        <div class="post-tags">
          {% for tag in post.tags %}
            <span class="post-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        <div class="post-meta">
          {% if post.reading_time %}
            <span>⏱️ {{ post.reading_time }} min</span>
          {% endif %}
          <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
        </div>
      </div>
    {% endfor %}
  </div>
  <div style="text-align: center; margin-top: 2rem;">
    <a href="{{ '/blog' | relative_url }}" style="font-size: 1.1rem; font-weight: 600; color: var(--secondary-color);">View All Posts →</a>
  </div>
</section>

<!-- Projects Section -->
<section id="projects">
  <h2>Featured Projects</h2>
  <div class="projects-grid">
    <div class="project-card">
      <h3>Agentic AI System Support Bot</h3>
      <p>
        A proof-of-concept chatbot that demonstrates agentic AI patterns using OpenAPI specifications as tools. 
        The agent autonomously orchestrates multiple tools to resolve user queries intelligently.
      </p>
      <div class="project-tags">
        <span class="project-tag">AI</span>
        <span class="project-tag">Agents</span>
        <span class="project-tag">Python</span>
      </div>
      <a href="#" class="project-link">Learn More →</a>
    </div>
    <div class="project-card">
      <h3>Real-time Data Pipeline</h3>
      <p>
        A production-grade Kafka and Spark Streaming based data pipeline handling millions of events. 
        Demonstrates microservices architecture and distributed data processing patterns.
      </p>
      <div class="project-tags">
        <span class="project-tag">Kafka</span>
        <span class="project-tag">Spark</span>
        <span class="project-tag">Scala</span>
      </div>
      <a href="#" class="project-link">Learn More →</a>
    </div>
    <div class="project-card">
      <h3>Coming Soon...</h3>
      <p>
        More exciting projects demonstrating complex agentic patterns, LLM applications, and system design. 
        Stay tuned!
      </p>
      <div class="project-tags">
        <span class="project-tag">LLMs</span>
        <span class="project-tag">Agents</span>
        <span class="project-tag">Open Source</span>
      </div>
      <a href="{{ '/blog' | relative_url }}" class="project-link">Read My Blog →</a>
    </div>
  </div>
</section>

<!-- Experience Section -->
<section id="experience">
  <h2>Professional Experience</h2>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
        <h3>Big Data Specialist</h3>
        <p class="position">Senior Engineer - Big Data & Streaming</p>
        <p class="duration">2018 - Present (8+ years)</p>
        <p>
          Architected and built scalable data pipelines using Scala, Spark, and Kafka. 
          Led microservices migration and ETL optimization projects. Recently pivoted to exploring Agentic AI.
        </p>
      </div>
    </div>
    <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
        <h3>Full Stack Developer</h3>
        <p class="position">Senior Engineer - Web Development</p>
        <p class="duration">2010 - 2018 (8 years)</p>
        <p>
          Built full-stack web applications using PHP and JavaScript. Designed and implemented REST APIs. 
          Gained deep understanding of system architecture and database design.
        </p>
      </div>
    </div>
    <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
        <h3>Early Career</h3>
        <p class="position">Software Developer</p>
        <p class="duration">2013 - 2018</p>
        <p>
          Started my journey in software development, learning fundamentals of programming, 
          web technologies, and software design patterns.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- Contact Section -->
<section id="contact">
  <div class="contact-section">
    <h2>Get In Touch</h2>
    <p style="font-size: 1.1rem; margin: 1.5rem 0;">
      I'd love to connect with fellow engineers, discuss AI/LLM projects, or collaborate on open-source initiatives.
    </p>
    <div class="social-links">
      <a href="{{ site.social_links.github }}" class="social-link" title="GitHub" target="_blank">👨‍💻</a>
      <a href="{{ site.social_links.linkedin }}" class="social-link" title="LinkedIn" target="_blank">💼</a>
      <a href="{{ site.social_links.twitter }}" class="social-link" title="Twitter" target="_blank">𝕏</a>
      <a href="{{ site.social_links.email }}" class="social-link" title="Email">✉️</a>
    </div>
    <p style="margin-top: 1.5rem; font-size: 0.95rem;">
      Email: <a href="mailto:your-email@example.com">your-email@example.com</a>
    </p>
  </div>
</section>
