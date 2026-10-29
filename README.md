\documentclass[9pt,letterpaper]{article}

% The reference PDF embeds CharterBT Roman/Bold/Italic.
\usepackage[left=0.43in,right=0.43in,top=0.25in,bottom=0.28in]{geometry}
\usepackage[T1]{fontenc}
\usepackage{charter}
\usepackage{titlesec}
\usepackage{enumitem}
\usepackage{tabularx}
\usepackage{array}
\usepackage[hidelinks]{hyperref}
\usepackage{microtype}

\pagestyle{empty}
\setlength{\parindent}{0pt}
\setlength{\parskip}{0pt}
\setlength{\tabcolsep}{0pt}
\setlength{\emergencystretch}{1em}

% Section heading and rule spacing.
\titleformat{\section}
  {\bfseries\normalsize}
  {}{0pt}{}
  [\vspace{-4pt}\rule{\textwidth}{0.35pt}]
\titlespacing*{\section}{0pt}{5.5pt}{4pt}

% Uniform bullet spacing throughout the document.
\setlist[itemize]{
  leftmargin=1.18em,
  label=\textbullet,
  itemsep=0.65pt,
  topsep=0pt,
  parsep=0pt,
  partopsep=0pt,
  itemindent=0pt
}

\newcommand{\resumeTwoCol}[2]{%
  \begin{tabularx}{\textwidth}{@{}>{\raggedright\arraybackslash}X>{\raggedleft\arraybackslash}p{0.27\textwidth}@{}}
    #1 & #2
  \end{tabularx}%
}
\newcommand{\project}[3]{%
  \resumeTwoCol{\textbf{#1}}{#2}\\[-1pt]
  {\itshape Tech Stack: #3}\par\vspace{-1pt}
}

\begin{document}
\fontsize{10}{12.8}\selectfont

% Header
\begin{center}
  {\fontsize{18}{14.7}\selectfont\bfseries Prem Kr Sah}\\[-1pt]
  +91-6001054097 \textbar\ \href{mailto:pksjuly721@gmail.com}{pksjuly721@gmail.com}\\[-1pt]
  \href{https://www.linkedin.com/in/prem-kr-sah/}{https://www.linkedin.com/in/prem-kr-sah/} \textbar\ \href{https://github.com/PremKr1122}{https://github.com/PremKr1122}
\end{center}
\vspace{-3pt}

\section*{Summary}
Computer Science and Engineering graduate and entry-level Data Analyst skilled in SQL, Python (Pandas, NumPy), Excel and Power BI. Experienced in data cleaning, validation, statistical and trend analysis on large datasets (228,000+ records), and in communicating insights through dashboards.

\section*{Skills}
\textbf{Programming \& Querying:} SQL (MySQL), Python, Pandas, NumPy, Data Modeling, Data Extraction, Data Validation\\[-1pt]
\textbf{Analysis \& Statistics:} EDA, Statistical Analysis, Regression, Trend Analysis, Outlier Analysis, Data Cleaning\\[-1pt]
\textbf{Visualization \& Reporting:} Power BI, DAX, Power Query, MS Excel, Dashboarding, Data Visualization\\[-1pt]
\textbf{Machine Learning \& NLP:} Scikit-Learn, Feature Engineering, Risk Prediction, NLTK, Sentiment Analysis\\[-1pt]
\textbf{Tools \& Frameworks:} FastAPI, REST APIs, Pydantic, Streamlit, PyTorch, Jupyter Notebook, Git, GitHub, Docker

\section*{Experience}
\resumeTwoCol{\textbf{Software Development Intern, Computer Vision \& AI} \hfill \hspace{7pt}\textbf{National Informatics Centre (NIC)}}{\textbf{July 2025 -- Aug 2025}}\\[-6pt]
\begin{itemize}
  \item Built a Python/FastAPI pipeline (InsightFace, PyMuPDF, regex) to extract and match voter IDs from semi-structured PDF records: 92.8\% ID extraction accuracy on 78 real records, 88.5\% face detection rate.
  \item Investigated extraction failures below these thresholds and identified two root causes -- missing voter photographs in source records and left-to-right, row-by-row extraction logic that broke on non-standard layouts -- to guide targeted fixes.
\end{itemize}
\vspace{3pt}
\resumeTwoCol{\textbf{Machine Learning Intern} \hfill \textbf{Feynn Labs}}{\textbf{Dec 2024 -- Feb 2025}}\\[-6pt]
\begin{itemize}
  \item K-Means market segmentation on 1,453 customer survey records identified 4 distinct customer segments.
  \item Conducted EDA (distribution and outlier analysis, box plots) and data cleaning (feature removal, one-hot encoding).
  \item Trained a mobile price prediction model on 988 records; Ridge regression achieved R\textsuperscript{2} = 0.48 on a 198-sample test set versus 0.36 for baseline Linear Regression.
\end{itemize}

\section*{Projects}
\project{Hotel Review Analytics Pipeline}{\href{https://github.com/PremKr1122/hotel-review-analytics-pipeline}{GitHub}}{Python, NLTK/VADER, MySQL, Power BI}
\begin{itemize}
  \item Analyzed 228,000+ hotel reviews with text (254,000+ loaded) across 10 cities for review- and aspect-level sentiment.
  \item Designed a normalized MySQL schema (hotels, reviews, review\_aspects); wrote SQL for KPIs, trends, and complaints.
  \item Validated pipeline integrity by reconciling review counts across ingestion, cleaning, and MySQL load stages, and resolved two data-loss bugs (encoding artifacts, malformed CSV field parsing) surfaced through automated logging and count audits.
  \item Delivered a two-page Power BI dashboard (DAX measures, city and date slicers); found 88.8\% of reviews positive and noise the weakest aspect (avg sentiment 0.23 vs 0.49 for cleanliness).
\end{itemize}
\vspace{3pt}
\project{Forest Fire Risk Analysis and Prediction}{\href{https://github.com/PremKr1122/Forest-fire-prediction}{GitHub}}{Python, Pandas, Scikit-Learn, FastAPI}
\begin{itemize}
  \item Explored 243 records via EDA, correlation-based feature selection, and scaling to identify key fire risk drivers.
  \item Compared Linear, Lasso, Ridge, and ElasticNet regression using 5-fold cross-validation; the final Ridge model achieved R\textsuperscript{2} of 0.9843 and MAE of 0.5642.
\end{itemize}
\vspace{3pt}
\project{Car Damage Prediction using Deep Learning}{\href{https://github.com/PremKr1122/Car_Damage_Prediction}{GitHub}}{PyTorch, ResNet50, Optuna, FastAPI}
\begin{itemize}
  \item Developed a ResNet50 transfer-learning classifier on 2,296 images across 6 damage classes; Optuna tuning (20 trials) improved validation accuracy from 82.58\% to 82.75\%, outperforming EfficientNet-B0.
\end{itemize}

\section*{Certifications}
\resumeTwoCol{\textbf{Data Visualization}, Tata}{Jul 2026}\\[-2pt]
\resumeTwoCol{\textbf{Data Science Job Simulation}, BCG}{Jan 2025}\\[-2pt]
\resumeTwoCol{\textbf{Machine Learning \& MLOps Bootcamp}, Udemy}{Oct 2024}

\section*{Education}
\resumeTwoCol{\textbf{Barak Valley Engineering College (BVEC), Assam}, B.Tech in Computer Science and Engineering}{\textbf{2022 -- 2026}}\\[-6pt]
\begin{itemize}
  \item \textbf{GPA: 7.63/10}
\end{itemize}

\end{document}
