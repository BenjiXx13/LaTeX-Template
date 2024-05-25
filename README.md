# LaTeX-Template
This repository contains a latex template for bachelor thesis.

## Sections, Sub-Sections, Sub-Sub-Sections
To have a nice overview within your .tex doc you can follow my commenting style.

```latex
% <><><><><><><><><><><><><><><><><><><><><><><><><>
% [ 1 ] [SEC]
% -- -- -- -- -- -- -- --
% 	TITEL:
%  -------
%	Ich bin ein Titel... 
% <><><><><><><><><><><><><><><><><><><><><><><><><>

\section{SECTION}

Text Text.



% <><><><><><><><><><><><><><><><><><><><><><><><><>
% [ 1.1 ] [SUB-SEC]
% -- -- -- -- -- -- -- --
% 	TITEL:
%  -------
%	Ich bin ein Titel... 
% <><><><><><><><><><><><><><><><><><><><><><><><><>
\subsection{SUB-SECTION}

Text Text.



% <><><><><><><><><><><><><><><><><><><><><><><><><>
% [ 1.1.1 ] [SUBSUB-SEC]
% -- -- -- -- -- -- -- --
% 	TITEL:
%  -------
%	Ich bin ein Titel... 
% <><><><><><><><><><><><><><><><><><><><><><><><><>
\subsubsection{SUBSUB-SEC}

Text Text.
```

## Acronyms
Acronyms are collected in a kind of table of content. How to use it?

```latex
# Go to abkuerzung-file.tex

# The longest acronym should go directly behind the begin statement
\begin{acronym}[HEREyourLONGESTacronym]

# Add a acronym to the list
\acro{usageInText}[AcroInTableOfContent]{fullWord}

# in the text you use the acronym the following way
\ac{usageInText}
\acf{usageInText} forces to show full acronym and text
\acs{usageInText} forces to show only acronym
\acl{usageInText} forces to show only the text of acronym
```

## Source Code
In some thesis there will be source code. I have configured some environments with the common programming languages like python and java.\
You can simply adjust the coloring. See also runnable.tex

Here is an example usage of source code...

```latex
\begin{java}[captionGoesInHere]{code:yourCustomReference}
	String returnString() {
    return "Hello there";
  }
\end{java}
```

## Table
You can simply create a table with the following code:

```latex
\begin{table}[h]
	\centering
	\caption[Caption]{\small Caption}
	\vspace{10pt}
	\begin{tabular}{|c|c|}% c=center,l=left,r=right
		\hline
		a & b\\
		\hline	
	\end{tabular}
\end{table}
```

## Graphics
Add graphics with the following code: 

```latex
\begin{center}
	\centering
	\includegraphics[width=\textwidth]{path.jpg}	
	\captionsetup{type=figure, list=no}
	\caption{\small caption}
  \label{fig_myFig}
\end{center}
```

Sometimes it is more usefull to use pdfs. Make sure your resolution is good enough!\
Also have in mind to always create a lable for your graphic to reference it in your text.


## Bibliography
These are possible entries for your biblopgraphy:

```latex
% Artikel zitieren 
@article{CiteTag,
  author   = {Nachname, Vorname},
  title    = {{Kapitel od Unterbeschreibung}},
  journal  = {Buch od. Haupttitel},
  pages    = {Seitenangabe der Quelle},
  year     = {2022}
  }

% Buch zitieren
@book{CiteTag,
  title     = {Titel des Buches},
  author    = {Nachname, Vorname},
  isbn.     = {Nummer},
  publisher = {Verlag},
  year      = {Erscheinungsjahr},
  length    = {436 pages} % Seitenanzahl des Buches
}

% Link Zitieren
@online{CiteTag,
  author   = {Nachname, Vorname},
  title    = {{Titel der Quelle} },
  year     = {Erscheinungsjahr},
  url      = {https://www.google.de},
  urldate  = {YYYY-MM-DD} % Datum, an dem auf Quelle zugegriffen wurde
}
% year = Jahr der Veröffentlichung
% urldate = Datum des Abrufs der Website
```
