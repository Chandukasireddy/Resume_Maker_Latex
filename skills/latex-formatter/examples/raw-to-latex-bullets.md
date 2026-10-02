# Raw to LaTeX Bullets Examples

A collection of 15+ before-and-after examples demonstrating how humanized text is converted into valid, properly escaped LaTeX code using standard macros and bold formatting.

---

## 1. Escaping Special Characters

### Example 1.1: Percentages & Metrics
- 📥 **Humanized Text:** *Engineered an automated data pipeline in Python, reducing execution time by 45% and processing 10K+ daily events.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Engineered an automated data pipeline in \textbf{Python}, reducing execution time by \textbf{45\%} and processing \textbf{10K+ daily events}.}
```

### Example 1.2: Ampersands in Tech Stacks
- 📥 **Humanized Text:** *Built a full-stack dashboard with React & Node.js, handling C# & C++ backend services.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Built a full-stack dashboard with \textbf{React \& Node.js}, integrating backend microservices engineered in \textbf{C\# \& C++}.}
```

### Example 1.3: Currency & Dollar Signs
- 📥 **Humanized Text:** *Optimized cloud resource allocation on AWS, cutting monthly infrastructure costs by $1,200.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Optimized cloud resource allocation on \textbf{AWS}, cutting monthly infrastructure costs by \textbf{\$1,200}.}
```

---

## 2. Technical Bolding & Keyword Formatting

### Example 2.1: Machine Learning / AI
- 📥 **Humanized Text:** *Developed a RAG pipeline with LangChain and PyTorch, achieving 94% precision on 5,000 PDF documents.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Developed a Retrieval-Augmented Generation (RAG) pipeline using \textbf{LangChain} and \textbf{PyTorch}, achieving \textbf{94\% precision} across a corpus of \textbf{5,000+ PDF documents}.}
```

### Example 2.2: REST APIs & Microservices
- 📥 **Humanized Text:** *Designed RESTful APIs using FastAPI and PostgreSQL, serving 500+ daily active users with sub-100ms latency.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Designed high-performance RESTful APIs using \textbf{FastAPI} and \textbf{PostgreSQL}, serving \textbf{500+ daily active users} with \textbf{sub-100ms latency}.}
```

### Example 2.3: DevOps & Containerization
- 📥 **Humanized Text:** *Containerized legacy applications using Docker and Kubernetes, reducing deployment time from 40 to 8 minutes.*
- 📄 **LaTeX Code:**
```latex
\resumeItem{Containerized application services using \textbf{Docker} and \textbf{Kubernetes}, streamlining CI/CD deployments and cutting setup time from 40 to \textbf{8 minutes}.}
```

---

## 3. Subheading & Project Formatting

### Example 3.1: Work Experience Entry
- 📥 **Raw Details:** *Software Engineer Intern at TechCorp Inc in San Francisco, CA (May 2023 to Aug 2023)*
- 📄 **LaTeX Code:**
```latex
\resumeSubheading
  {Software Engineer Intern}{May 2023 -- Aug 2023}
  {TechCorp Inc.}{San Francisco, CA}
  \resumeItemListStart
    \resumeItem{Engineered asynchronous background tasks using \textbf{Celery} and \textbf{Redis}, boosting worker queue throughput by \textbf{30\%}.}
    \resumeItem{Refactored core authentication modules in \textbf{TypeScript}, eliminating 15+ legacy security vulnerabilities.}
  \resumeItemListEnd
```

### Example 3.2: Project Entry
- 📥 **Raw Details:** *Autonomous Robot Navigator project built with ROS, C++, and OpenCV (Jan 2024 - Apr 2024)*
- 📄 **LaTeX Code:**
```latex
\resumeProjectHeading
  {\textbf{Autonomous Robot Navigator} $|$ \emph{ROS, C++, OpenCV, Python}}{Jan 2024 -- Apr 2024}
  \resumeItemListStart
    \resumeItem{Implemented real-time obstacle avoidance algorithms in \textbf{C++}, processing LiDAR sensor data at \textbf{60 FPS}.}
    \resumeItem{Simulated complex urban navigation environments in \textbf{Gazebo}, achieving \textbf{98\% collision-free path accuracy}.}
  \resumeItemListEnd
```
