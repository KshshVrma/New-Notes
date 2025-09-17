
[[To_do]]
code for Jake's resume : https://www.overleaf.com/project/688631246369ef0840a9dd43


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
  \small Lucknow, India $|$ 8795662299 $|$ \href{mailto:kashishverma8382@gmail.com}{\underline{kashishverma8382@gmail.com}} \\
  \href{https://www.linkedin.com/in/kashish-verma-342347221/}{\underline{LinkedIn}} $|$
  \href{https://github.com/KshshVrma}{\underline{GitHub}} $|$
  \href{https://leetcode.com/Kashish_024/}{\underline{Leetcode}} $|$
  \href{https://www.codechef.com/users/another_year}{\underline{CodeChef}}
\end{center}

%-----------EDUCATION-----------
\section{Education}
\resumeSubHeadingListStart
  \resumeSubheading
    {SRM Institute of Science and Technology (SRMIST)}{Kattankulathur, India}
    {B.Tech, CGPA: 9.65}{2019 -- 2024}
  \resumeSubheading
    {DPS Eldeco}{Lucknow, India}
    {Class 12 – 86.4\%}{2018}
  \resumeSubheading
    {DPS Eldeco}{Lucknow, India}
    {Class 10 – 91.2\%}{2016}
\resumeSubHeadingListEnd

%-----------EXPERIENCE-----------
\section{Internships}
\resumeSubHeadingListStart
  \resumeSubheading
    {Web Development Intern – Brainovision Solutions}{Remote}
    {Tech Stack: HTML, CSS, JavaScript, ReactJS}{Aug. 2022 – Sep. 2022}
  \resumeSubheading
    {Data Analytics Virtual Internship – EduSkills}{Remote}
    {Analyzed datasets and extracted insights using tools on AWS}{May 2023 – July 2023}
\resumeSubHeadingListEnd

%-----------PROJECTS-----------
\section{Projects}
\resumeSubHeadingListStart
  \resumeProjectHeading{\textbf{News Headlines Website} $|$ \emph{ReactJS}}{}
    \resumeItemListStart
      \resumeItem{Displays recent news headlines.}
      \resumeItem{\href{https://64d9153b7408bc39a589c8c7--dreamy-toffee-a4a189.netlify.app/}{Live Demo}}
    \resumeItemListEnd

  \resumeProjectHeading{\textbf{eNotes App} $|$ \emph{MongoDB, ReactJS}}{}
    \resumeItemListStart
      \resumeItem{Online note-taking app with add, edit, and delete functionality.}
      \resumeItem{\href{https://kshshvrma.github.io/eNotes/}{Live Demo}}
    \resumeItemListEnd

  \resumeProjectHeading{\textbf{Gym Website} $|$ \emph{ReactJS}}{}
    \resumeItemListStart
      \resumeItem{Displays exercises based on target muscle group.}
      \resumeItem{\href{https://eloquent-axolotl-8ed967.netlify.app/}{Live Demo}}
    \resumeItemListEnd
\resumeSubHeadingListEnd

%-----------SKILLS-----------
\section{Technical Skills}
\begin{itemize}[leftmargin=0.15in, label={}]
  \small{\item{
    \textbf{Languages}{: C++, C, Python, JavaScript, SQL} \\
    \textbf{Frameworks \& Libraries}{: ReactJS, NodeJS, MongoDB, HTML/CSS, Express.js} \\
    \textbf{Tools}{: Git, VS Code, AWS (Basics)}
  }}
\end{itemize}

%-----------COURSES-----------
\section{Courses}
\begin{itemize}
  \item Design and Analysis of Algorithms (Top 1\%) – NPTEL
  \item DBMS (Elite + Top 2\%) – NPTEL
  \item Getting Started with Data Analytics on AWS – Coursera
  \item Soft Skills and Personality (Top 5\%) – NPTEL
\end{itemize}

%-----------OPEN SOURCE-----------
\section{Open Source Contributions}
\begin{itemize}
  \item \textbf{C-Simplify:} Improved design and responsiveness. \href{https://github.com/lovishprabhakar/C-Simplify}{GitHub}
  \item \textbf{Sudo-Clone:} Helped develop Instagram clone. \href{https://github.com/sandeep-ahirwar/sudo-clones}{GitHub}
\end{itemize}

%-----------ACHIEVEMENTS-----------
\section{Achievements}
\begin{itemize}
  \item Solved 800+ problems on CodeChef, Leetcode, GFG, Codeforces
  \item CodeChef Global Rank 307 (Starters 57), Rank 433 (Starters 53)
  \item 3-Star at CodeChef, Pupil at Codeforces
\end{itemize}


\end{document}




____________________________________________________________________
second: 
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
  \small Lucknow, India $|$ 8795662299 $|$ \href{mailto:kashishverma8382@gmail.com}{\underline{kashishverma8382@gmail.com}} \\
  \href{https://www.linkedin.com/in/kashish-verma-342347221/}{\underline{LinkedIn}} $|$
  \href{https://github.com/KshshVrma}{\underline{GitHub}} $|$
  \href{https://leetcode.com/Kashish_024/}{\underline{Leetcode}} $|$
  \href{https://www.codechef.com/users/another_year}{\underline{CodeChef}}
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
  \item \textbf{Software Engineer 1}, Serko Ltd., Bengaluru \hfill \emph{Jan 2025 – Present}\\
    \begin{itemize}
      \item Bullet‑point 1 here
      \item Bullet‑point 2 here
    \end{itemize}

  \item \textbf{Software Engineer 1}, Sabre, Bengaluru \hfill \emph{Aug 2024 – Jan 2025}\\
    \begin{itemize}
      \item …
    \end{itemize}
    \item \textbf{Software Engineer Intern}, Sabre, Bengaluru \hfill \emph{Jan 2024 – Jul 2024}\\
    \begin{itemize}
      \item …
    \end{itemize}
\end{itemize}

%-----------PROJECTS-----------
\section{Projects}
\resumeSubHeadingListStart
  \resumeProjectHeading{\textbf{News Headlines Website} $|$ \emph{ReactJS}}{}
    \resumeItemListStart
      \resumeItem{Displays recent news headlines.}
      \resumeItem{\href{https://64d9153b7408bc39a589c8c7--dreamy-toffee-a4a189.netlify.app/}{Live Demo}}
    \resumeItemListEnd

  \resumeProjectHeading{\textbf{Product Comparator} $|$ \emph{Spring Boot}}{}
    \resumeItemListStart
      \resumeItem{Compares Products across different e-commerce sites and provides recommendations based on LLM.}
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
\begin{itemize}
  \item Design and Analysis of Algorithms (Top 1\%) – NPTEL
  \item DBMS (Elite + Top 2\%) – NPTEL
  \item Soft Skills and Personality (Top 5\%) – NPTEL
  \item Certified Application Developer - ServiceNow
\end{itemize}


%-----------ACHIEVEMENTS-----------
\section{Achievements}
\begin{itemize}
  \item Solved 1000+ problems on CodeChef, Leetcode, GFG, Codeforces
  \item CodeChef Global Rank 307 (Starters 57), Rank 433 (Starters 53)
  \item Contributed in Hacktoberfest 2022
  \item 1000+ commits across 90+ github repositories
\end{itemize}


\end{document}
