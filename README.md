`conda create --file environment.yml`

# 3. Distribution of Fourier coefficients vs the Gaussian assumption


**In a nutshell.** Test the Gaussian assumption at the heart of the PTA likelihood. Simulate the Fourier coefficients of the timing residuals produced by a population of SMBHBs and compare their distribution, bin by bin, against the Gaussian that the standard likelihood assumes. You should find approximate Gaussianity at low frequency breaking down into heavy-tailed, high-kurtosis behavior at high frequency, where a few loud binaries dominate each bin.


**MVP → stretch. MVP:** strain-level (earth-term) coefficients — draw a population, sum sinusoids with random phases over many realizations, and   compare the normalized coefficients per bin to a unit Gaussian (QQ plots, kurtosis vs frequency). Stretch: fold in the pulsar response and test whether the non-Gaussian tail biases a standard power-law recovery.


**Get this right.** Match the comparison Gaussian’s variance to the sample variance in each bin, then test the shape — otherwise a wrong variance masquerades as non-Gaussianity.


*References.*
  - Lamb, Wachter, Mitridate, Sardesai, Bécsy, Hagen, Taylor & Kelley 2025, arXiv:2511.09659 (Finite Populations & Finite Time: the non-Gaussianity of a GW background).
  - Sato-Polito & Zaldarriaga 2025, PRD 111, 023043 (amplitude distribution / heavy tails).
  - Xue, Pan & Dai 2025, PRD 111, 043022 (non-Gaussian statistics of nanohertz GWs).
  - Bernardo, Appleby & Ng 2024, JCAP 01, 017 (toward a test of Gaussianity).


**Software.** holodeck (populations); numpy / scipy (the MVP needs little else); enterprise (stretch).
