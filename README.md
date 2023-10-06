# QOSF Quantum Computing Mentorship Program
<img src="qosf.png" width="30%" />

## Cohort 8 Screening Tasks - Task 3: Decomposition
Using the $U$ and $CX$ gates shown below, decompose the matrices to obtain $CCX$ and $CCCX$ gates. As a bonus, create a method for constructing any multi-controlled $X$ gate.

$$
U(\theta,\phi,\lambda)=
\begin{pmatrix} 
\cos \frac{\theta}{2}\ & -e^{i\lambda} \sin \frac{\theta}{2}\ \\\ 
e^{i\phi} \sin \frac{\theta}{2}\ & e^{i(\phi+\lambda)} \cos \frac{\theta}{2}\ 
\end{pmatrix}
$$

$$
CX=\begin{pmatrix} 
1 & 0 & 0 & 0 \\\ 
0 & 1 & 0 & 0 \\\ 
0 & 0 & 0 & 1 \\\ 
0 & 0 & 1 & 0 
\end{pmatrix}
$$

$$
CCX=\begin{pmatrix} 
1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\\ 
0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\\ 
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\\ 
0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\\ 
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\\
0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 \\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 
\end{pmatrix}
$$

$$
CCCX=\begin{pmatrix} 
1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\\ 
0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\ 
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\ 
0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\ 
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1\\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0
\end{pmatrix}
$$

## 1. Decompostion of the I (= Identity) and the X (= NOT) gates using the U gate 
$$\eqalign{
U(0,0,0) & = \begin{pmatrix} 
             \cos 0 & -e^{0} \sin 0 \\\ 
             e^{0} \sin 0 & e^{0} \cos 0 
             \end{pmatrix} \\
         & = \begin{pmatrix} 
             1 & 0 \\\ 
             0 & 1 
             \end{pmatrix}
}$$

$$
\therefore I=U(0,0,0)
$$

$$\eqalign{
U(\pi,-\frac{\pi}{2}\,\frac{\pi}{2}\) & = \begin{pmatrix} 
                                          \cos \frac{\pi}{2}\ & -e^{i\frac{\pi}{2}\} \sin \frac{\pi}{2}\ \\\ 
                                          e^{-i\frac{\pi}{2}\} \sin \frac{\pi}{2}\ & e^{0} \cos \frac{\pi}{2}\ 
                                          \end{pmatrix} \\
                                      & = \begin{pmatrix} 
                                          0 & -e^{i\frac{\pi}{2}\} \\\ 
                                          e^{-i\frac{\pi}{2}\} & 0 
                                          \end{pmatrix} \\
                                      & = \begin{pmatrix} 
                                          0 & -\cos \frac{\pi}{2}\ - i \sin \frac{\pi}{2}\ 
                                          \cos (-\frac{\pi}{2}\) + i \sin (-\frac{\pi}{2}\)  & 0 
                                          \end{pmatrix} \\
                                      & = \begin{pmatrix} 
                                          0 & -i \\\ 
                                          -i & 0 
                                          \end{pmatrix} \\
                                      & = RX(\pi) \\
                                      & = -i X
}$$

$$
\therefore X=i U(\pi,-\frac{\pi}{2}\,\frac{\pi}{2}\) 
$$

## 2. Decomposition of the CX gate using the I and the X gates
$$
CX = \ket{0} \bra{0} \otimes I + \ket{1} \bra{1} \otimes X \\
$$

## 3. Decomposition of the CCX gate using the I and the CX gates
$$
CCX = \ket{0} \bra{0} \otimes I \otimes I + \ket{1} \bra{1} \otimes CX \\
$$

## 4. Decomposition of the CCCX gate using the I and the CCX gates
$$
CCCX = \ket{0} \bra{0} \otimes I \otimes I \otimes I + \ket{1} \bra{1} \otimes CCX 
$$

