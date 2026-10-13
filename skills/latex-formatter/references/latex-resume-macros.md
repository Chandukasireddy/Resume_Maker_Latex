# LaTeX Resume Macros Reference

Standardized LaTeX macros and environments used in clean, ATS-friendly resume templates.

---

## 1. Core Resume Environment Macros

Most modern LaTeX resume templates (such as Jake's Resume or minimal ATS templates) use custom macros to maintain consistent layout alignment.

### Subheading Macro (`\resumeSubheading`)
Renders an entry with 4 parameters: Title, Date, Subtitle/Company, Location.

```latex
\newcommand{\resumeSubheading}[4]{
  \vspace{-1pt}\item
    \begin{table*}[t]
      \leftskip=0in
      \rightskip=0in
      \begin{tabular*}{\textwidth}[t]{l@{\extracolsep{\fill}}r}
        \textbf{#1} & #2 \\
        \textit{\small#3} & \textit{\small #4} \\
      \end{tabular*}
    \end{table*}\vspace{-7pt}
}
```

#### Usage Example (Anonymized):
```latex
\resumeSubheading
  {Software Engineer Intern}{May 2023 -- Aug 2023}
  {TechCorp Inc.}{San Francisco, CA}
```

---

### Project Heading Macro (`\resumeProjectHeading`)
Renders a project title with its tech stack on the left and date on the right.

```latex
\newcommand{\resumeProjectHeading}[2]{
    \item
    \begin{tabular*}{\textwidth}{l@{\extracolsep{\fill}}r}
      \small#1 & #2 \\
    \end{tabular*}\vspace{-7pt}
}
```

#### Usage Example (Anonymized):
```latex
\resumeProjectHeading
  {\textbf{Autonomous Robot Navigator} $|$ \emph{Python, ROS, C++, OpenCV}}{Jan 2024 -- Apr 2024}
```

---

### Item Macro (`\resumeItem`)
Formats individual bullet points with tight spacing.

```latex
\newcommand{\resumeItem}[1]{
  \item\small{
    {#1 \vspace{-2pt}}
  }
}
```

#### Usage Example:
```latex
\resumeItem{Engineered a high-throughput REST API using \textbf{FastAPI} and \textbf{PostgreSQL}, handling over \textbf{10K+ daily requests} with \textbf{99.9\% uptime}.}
```

---

## 2. List Structure Environments

Always wrap subheadings and items in list environments:

```latex
% Top-level list for sections
\newcommand{\resumeSubHeadingListStart}{\begin{itemize}[leftmargin=0.0in, label={}]}
\newcommand{\resumeSubHeadingListEnd}{\end{itemize}}

% Inner list for bullet points
\newcommand{\resumeItemListStart}{\begin{itemize}}
\newcommand{\resumeItemListEnd}{\end{itemize}\vspace{-5pt}}
```

### Full Nested Structure:
```latex
\resumeSubHeadingListStart
  \resumeSubheading
    {Software Engineer Intern}{May 2023 -- Aug 2023}
    {TechCorp}{San Francisco, CA}
    \resumeItemListStart
      \resumeItem{Architected microservices backend...}
      \resumeItem{Optimized SQL query performance...}
    \resumeItemListEnd
\resumeSubHeadingListEnd
```

---

## 3. Section Header Formatting

Customizing section headers using `titlesec`:

```latex
\titleformat{\section}{
  \vspace{-4pt}\scshape\raggedright\large
}{}{0em}{}[\color{black}\titlerule \vspace{-5pt}]
```

Usage:
```latex
\section{Education}
\section{Technical Skills}
\section{Experience}
\section{Projects}
```
