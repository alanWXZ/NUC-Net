# NUC-Net: Non-uniform Cylindrical Partition Network for Efficient LiDAR Semantic Segmentation




## Project Overview
NUC-Net is a network based on non-uniform cylindrical partitioning for efficient LiDAR semantic segmentation. This method overcomes the high computational cost of traditional -based approaches by adaptively partitioning point cloud data, significantly improving the efficiency and accuracy of LiDAR point cloud processing in large-scale environments.

## Updates
- The code will be publicly released soon. Stay tuned.
- **Non-uniform Cylindrical Partition**: An adaptive partitioning method to better capture the geometric structure of LiDAR point clouds.
- **Nonuniform Multi-scale Aggregation**: A novel feature aggregation technique that dynamically adjusts receptive fields based on spatial distribution.
- **Instance Augmentation**: A data augmentation strategy designed to enhance the robustness of instance-level segmentation.

## Features
- Non-uniform cylindrical partitioning strategy
- Faster and more accurate processing of LIDAR point cloud
- A few lines of code are enough to bring a significant improvement.


\begin{table}
	\setlength\tabcolsep{3pt}
	\footnotesize
	
\begin{center}	
	%\resizebox{\linewidth}{!}{
	\begin{tabular}{c|c|c|c}
		\hline
		
		Methods&Partition Mechanism&Voxel Resolution&{mIoU}\\
		\hline																				
		\multirow{6}*{PolarNet
			~\cite{LiDAR_PolarNet}}&\multirow{3}*{Uniform}&[120,180,32] &52.1\\
		&&[120,360,32] &52.6\\
		
		&&[480,360,32]&54.9 \\
		
		&\multirow{3}*{Non-uniform (API)}&[120,180,32]&57.6 (\textbf{+5.5}) \\
		
		&&[120,360,32]&58.7 (\textbf{+6.1}) \\
		&&[480,360,32]&59.6 (\textbf{+4.7}) \\ 
		\hline				
		\multirow{6}*{Cylinder3D
			~\cite{LiDAR_Cylindrical}}&\multirow{3}*{Uniform}&[120,180,32] &59.8\\
		&&[120,360,32] &61.8\\
		
		&&[480,360,32]& 64.5\\
		
		&\multirow{3}*{Non-uniform (API)}&[120,180,32]&65.6 (\textbf{+5.8}) \\
		
		&&[120,360,32]& 66.5 (\textbf{+4.7})\\
		&&[480,360,32]&66.8 (\textbf{+2.3}) \\
		
		\hline
	\end{tabular}
	%}
	\end{center}
	\caption{Results of before and after exploiting the non-uniform partition method on PolarNet and Cylinder3D. `Uniform' represents the uniform partition methods proposed by PolarNet~\protect\cite{LiDAR_PolarNet} or Cylinder3D~\protect\cite{LiDAR_Cylindrical}. `Non-uniform' represents the proposed non-uniform partition(Arithmetic Progression of Interval) method. }
	\label{tab:generality}
	\vspace{-0.5cm}
\end{table}

## Installation
