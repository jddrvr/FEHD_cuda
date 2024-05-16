# FEHD_cuda
FEHD algorithm written for nvidia gpus.

Executes the FEHD algorithm on a user provided time series. The input
file must be columns as channels, time points as rows. Trials or
epochs must all be the same length. Epoch boundaries are not indicated
in the input file.  The program will assume that every epochPts is a
new epoch. It is recommended that the total number of time points in
the data file divide the epoch length exactly. The included mechanism
to deal with this is the basic chop.

Installation/ compilation:

enter the directory and type 'make'. If it fails it likely means that
the compiler cannot find the requested libraries. Make sure you have
them, and adapt the makefile as needed.  When you have an executable,
put it in your path.

Requires: cublas, cusolver, blas, lapacke

Use:
FEHD -filename <data filename> -sampRate <sampling rate of data> -epochPts <time points in an epoch or trial> -numPCs <number of principal components to use> -numLags <number of lags in the AR model> -freqLo <low freq bound> -freqHi <high freq bound> -numFreqs <how many freqs to evaluate> -numParticles <number of solvers in parallel> -outfolder <where to put the output>



pull requests are welcome.  

