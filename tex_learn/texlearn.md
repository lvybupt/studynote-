#tex-learning note

####多图并列排版

```
\begin{figure*}	\renewcommand{\captionfont}{\footnotesize}	\centering	\subfigure[Result of Route Sample 3(a) in Table 2]	{\label{fig6:subfig:a}		\includegraphics[width=8.55cm,height=6cm]{foot}} 	\subfigure[Result of Route Sample 3(b) in Table 2]	{\label{fig6:subfig:b}		\includegraphics[width=8.55cm,height=6cm]{bike}}	\subfigure[Result of Route Sample 3(c) in Table 2]	{\label{fig6:subfig:c}		\includegraphics[width=8.55cm,height=6cm]{bus}}	\subfigure[Result of Route Sample 3(d) in Table 2]	{\label{fig6:subfig:d}		\includegraphics[width=8.55cm,height=6cm]{car}}	\caption{Experiment Results of our DBSR algorithm on different routes}\end{figure*}

```