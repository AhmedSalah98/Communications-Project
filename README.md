# Communications-Project
Different modulation schemes, BPSK, QPSK, FSK, QAM (16-64) simulation in an AWGN environment.

## BPSK (Binary Phase Shift Keying modulation) :
Two phase modulation scheme, where the 0’s and 1’s in a binary message are represented by two different phase states in the carrier signal: θ=0∘ for binary 1 and θ=180∘ for binary 0.

* Scheme Diagram :
* Scatter plot before noise :
* Scatter plot after noise :
* BER figure :

## QPSK (Quadrature Phase Shift Keying modulation)  :
Phase modulation technique, in which two information bits (combined as one symbol) are modulated at once, selecting one of the four possible carrier phase shift states.

* Scheme Diagram :
* Scatter plot before noise :
* Scatter plot after noise :
* BER figure :

## FSK (Frequency Shift Keying modulation)  :
Frequency modulation scheme, in which digital information is transmitted through discrete frequency changes of a carrier signal.

* Scheme Diagram :
* Scatter plot before noise :
* Scatter plot after noise :
* BER figure :

## QAM (Quadrature Amplitude Modulation)  :
QAM is a method of combining two amplitude-modulated (AM) signals into a single channel, thereby doubling the effective bandwidth.

#### QAM 16:
* Scheme Diagram :
* Scatter plot before noise :
* Scatter plot after noise :
* BER figure :

#### QAM 64:
* Scheme Diagram :
* Scatter plot before noise :
* Scatter plot after noise :
* BER figure :

# General instructions to reproduce figures:
1. Start Matlab then create a new Simulink model.
2. Open the Simulink library browser then drag and drop blocks and connect them (as shown in Scheme Diagrams of each modulation scheme).
3. Set number of frames to 10000 
4. Set Sample time to 1 and Samples per frame to 100 and intial seed to 37 for the Random Integers Generator.
5. Set intial seed to 67 for the AWGN Channel.
6. Set output data to Port for Error Rate Calculation.
7. Special Parameters: 
  * BPSK : Set M-ary number to 2 for the Integer Generator and Phase offset to 0 for the modulator and demodulator.
  * QPSK : Set M-ary number to 4 for the Integer Generator and Phase offset to pi/4 for the modulator and demodulator.
  * FSK : Set M-ary number to 2 for the Integer Generator and the FSK modulator and demodulator.
  * QAM 16 : Set M-ary number to 16 for the Integer Generator and the FSK modulator and demodulator and set Normalization method to                  Average Power.
  * QAM 64 : Set M-ary number to 64 for the Integer Generator and the FSK modulator and demodulator and set Normalization method to                  Average Power.
8. press run to reproduce the scatter plot figures.
9. To reproduce the BER figure enter the command "bertool" then press "plot" to plot the exact figure then press "Monte Carlo" tab and      enter the range [-10, 10], the path to slx file and variable name then press "Run".
