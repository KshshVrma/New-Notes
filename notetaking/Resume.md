\documentclass[letterpaper,11pt]{article}

\usepackage{latexsym}
\usepackage[empty]{fullpage}
\usepackage{titlesec}
\usepackage{marvosym}
\usepackage[usenames,dvipsnames]{color}
\usepackage{enumitem}
\usepackage[hidelinks]{hyperref}
\usepackage{fancyhdr}
\usepackage[english]{babel}
\usepackage{tabularx}
\input{glyphtounicode}

\pagestyle{fancy}
\fancyhf{}
\fancyfoot{}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}

\addtolength{\oddsidemargin}{-0.5in}
\addtolength{\textwidth}{1in}
\addtolength{\topmargin}{-.5in}
\addtolength{\textheight}{1.0in}

\urlstyle{same}
\raggedbottom
\raggedright
\setlength{\tabcolsep}{0in}

\titleformat{\section}{
  \vspace{-4pt}\scshape\raggedright\large
}{}{0em}{}[\color{black}\titlerule \vspace{-5pt}]

\pdfgentounicode=1

\newcommand{\resumeItem}[1]{\item\small{{#1 \vspace{-2pt}}}}
\newcommand{\resumeSubheading}[4]{
  \vspace{-2pt}\item
  \begin{tabular*}{0.97\textwidth}[t]{l@{\extracolsep{\fill}}r}
    \textbf{#1} & #2 \\
    \textit{\small#3} & \textit{\small #4} \\
  \end{tabular*}\vspace{-7pt}
}
\newcommand{\resumeProjectHeading}[2]{
  \item
  \begin{tabular*}{0.97\textwidth}{l@{\extracolsep{\fill}}r}
    \small#1 & #2 \\
  \end{tabular*}\vspace{-7pt}
}
\newcommand{\resumeSubHeadingListStart}{\begin{itemize}[leftmargin=0.15in, label={}]}
\newcommand{\resumeSubHeadingListEnd}{\end{itemize}}
\newcommand{\resumeItemListStart}{\begin{itemize}}
\newcommand{\resumeItemListEnd}{\end{itemize}\vspace{-5pt}}

\begin{document}

\begin{center}
  \textbf{\Huge \scshape Kashish Verma} \\ \vspace{1pt}
\small Lucknow, India $\cdot$ +91-8795662299 $\cdot$ \href{mailto:kashishverma8382@gmail.com}{kashishverma8382@gmail.com}
 \\
\href{https://www.linkedin.com/in/kashish-verma-342347221/}{LinkedIn} $\cdot$ 
\href{https://github.com/KshshVrma}{GitHub (90+ Repos)} $\cdot$ 
\href{https://leetcode.com/Kashish_024/}{Leetcode (750+)} $\cdot$ 
\href{https://www.codechef.com/users/another_year}{CodeChef (3*)}

\end{center}

%-----------SKILLS-----------
\section{Technical Skills}
\begin{itemize}[leftmargin=0.15in, label={}]
  \small{\item{
    \textbf{Languages \& Frameworks:} Java, SQL, Python, Spring Boot, JUnit \\
    \textbf{Cloud \& DevOps:} GCP, Jenkins, Docker (basic), Git, CI/CD, IntelliJ, Postman \\
    \textbf{Databases \& Concepts:} Oracle DB, H2, REST APIs, Microservices, SAML2, Agile
  }}
\end{itemize}


%-----------EXPERIENCE-----------
\section*{Experience}
\begin{itemize}[leftmargin=*]

  \item \textbf{Software Engineer 1}, Serko Ltd., Bengaluru \hfill \emph{Jan 2025 -- Present}
    \begin{itemize}
      \item Strengthened platform security by redesigning encryption logic across distributed services, improving data protection and compliance.
      \item Led automated report generation and cleanup during a customer-impacting P0 incident, reducing manual overhead and ensuring rapid recovery.
    \end{itemize}

  \item \textbf{Software Engineer 1}, Sabre, Bengaluru \hfill \emph{Aug 2024 -- Jan 2025}
    \begin{itemize}
      \item Delivered critical security patches to production APIs, preventing known vulnerabilities and aligning with internal compliance standards.
      \item Developed shell and Python scripts for automating database extracts, reducing manual developer effort by ~50\%.
    \end{itemize}

  \item \textbf{Software Engineer Intern}, Sabre, Bengaluru \hfill \emph{Jan 2024 -- Jul 2024}
    \begin{itemize}
      \item Resolved a critical booking system bug that impacted nearly 50\% of transactions, improving user experience and restoring booking accuracy.

    \end{itemize}

\end{itemize}

%-----------PROJECTS-----------
\section{Projects}
\resumeSubHeadingListStart

  \resumeProjectHeading{\textbf{Product Comparator} $|$ \emph{Spring Boot}}{}
    \resumeItemListStart
      \resumeItem{Integrated LLM-based recommendation engine using Gemini API and Spring Boot to compare product listings from Amazon, Flipkart}
      \resumeItem{\href{https://github.com/KshshVrma/Product-Comparator}{Repository}}
    \resumeItemListEnd

  \resumeProjectHeading{\textbf{Code Vulnerability Detector} $|$ \emph{Python}}{}
    \resumeItemListStart
      \resumeItem{Scans GitHub Repositories to find Vulnerabilities in the code.}
      \resumeItem{\href{https://code-vulnerability-detector-wldhxxbvf367hfxap4gxti.streamlit.app/}{Live Demo}}
    \resumeItemListEnd
\resumeSubHeadingListEnd


%-----------EDUCATION-----------
\section{Education}
\resumeSubHeadingListStart
  \resumeSubheading
    {SRM Institute of Science and Technology (SRMIST)}{Kattankulathur, India}
    {B.Tech in Computer Science Engineering \quad \textbar \quad CGPA: 9.68/10}{2020 -- 2024}
\resumeSubHeadingListEnd

%-----------COURSES-----------
\section{Certifications}
\begin{itemize}[leftmargin=*]
  \item NPTEL: DAA (Top 1\%), DBMS (Elite + Top 2\%), Soft Skills (Top 5\%)
  \item Certified Application Developer – ServiceNow
\end{itemize}


%-----------ACHIEVEMENTS-----------
\section{Achievements}
\begin{itemize}
  \small{\item Solved 1000+ problems on CodeChef, Leetcode, GFG, Codeforces
  \item CodeChef Global Rank 307 (Starters 57), Rank 433 (Starters 53)
  \item 1000+ commits across 90+ Github repositories
  \item Received performance-based scholarship twice and published 2 research papers in scopus-indexed journals
   \item Contributed in Hacktoberfest 2022 with meaningful open-source contributions}
\end{itemize}


\end{document}
