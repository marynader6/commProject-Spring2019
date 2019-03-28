# BPSK Modulation scheme
## Explanation
Binary Phase Shift Keying (BPSK) is a type of digital modulation technique in which we are sending one bit per symbol i.e., ‘0’ or ‘1’.It is a two phase modulation scheme, where the 0’s and 1’s in a binary message are represented by two different phase states in the carrier signal: θ=0∘ for binary 1 and θ=180∘ for binary 0.
s1(t)=Ac cos(2πfct),0≤t≤Tb for binary 1
s0(t)=Ac cos(2πfct+π),0≤t≤Tb for binary 0
        


## Instructions
- To get blocks click on the model (white sketch ) and write name of the block you want. we will get 
  - Random integer generator   
  - BPSK Modulator Baseband
  - AWGN channel
  - BPSK Demodulator Baseband
  - Error rate calculation
  - Display : will show you three values. The first value is the BER, the second value is the number of incorrect bits, and the               third value is the total number of bits received).
  - 2* Constellation diagram (It is a representation of a signal modulated by a digital modulation scheme .It displays the signal as a two-dimensional xy-plane scatter diagram in the complex plane at symbol sampling instants. The angle of a point, measured counterclockwise from the horizontal axis, represents the phase shift of the carrier wave from a reference phase.).
  - To workspace (choose variable name) (used to get BER vs Eb/No figure)
- Connect them in the same order they'd listed **except**
  - Random generator: connect it with **Error rate calculation** also
  - Error rate calculation: connect it to **To workspace** 
  - Constellation diagram: connect one before AWGN channel and the other after the channel
- Double click on Random integer generator ,change **M-ary number** to 2.
- Double click on error rate calculation block and in **output data** choose port instead of workspace,so you can connect the               Display block.
- Double click on To workspace block change **limit data points to last** to 2, then **save format** to array, 
  then **save 2-D signals as** choose 2-D array.
- To run the model and see the scatter plots click on run button.
- To get BER vs Eb/No figure:
  - Double click on AWGN channel and change “Eb/No” to EbNo
  - In command window of matlab write bertool 
  - Change Eb/No range to -10:10
  - Click on “Monte Carlo” tab
  - Change Eb/No range to -10:.5:10, browse and choose your simulink model, write variable name of **To workspace** block,  then click on run
  
## Scatter plot
### Before Noise
![BPSKB](https://github.com/marynader6/commProject-Spring2019/blob/master/BPSKB.PNG)
### After Noise
![BPSKA](https://github.com/marynader6/commProject-Spring2019/blob/master/BPSKAfter.PNG)

## BER performance figure
![BPSKber](https://github.com/marynader6/commProject-Spring2019/blob/master/BPSK.png)

# QPSK Modulation scheme
## Explanation
Quadrature Phase Shift Keying (QPSK)or sometimes called as 4-PSK is a form of Phase Shift Keying in which two bits are modulated at once, selecting one of four possible carrier phase shifts (0, 90, 180, or 270 degrees). QPSK allows the signal to carry twice as much information as ordinary PSK using the same bandwidth. 

## Instructions
They are the same as BPSK except some changes:
- QPSK modulator and demodulator blocks
- Double click on Random integer generator ,change **M-ary number** to 4.

## Scatter plot
### Before Noise
![QPSKB](https://github.com/marynader6/commProject-Spring2019/blob/master/QPSKB.PNG)
### After Noise
![QPSKA](https://github.com/marynader6/commProject-Spring2019/blob/master/QPSKA.PNG)

## BER performance figure
![QPSKber](https://github.com/marynader6/commProject-Spring2019/blob/master/QFSK.png)

# FSK Modulation scheme
## Explanation
Frequency-shift keying (FSK) is a frequency modulation scheme in which digital information is transmitted through discrete frequency changes of a carrier signal.The output of a FSK modulated wave is high in frequency for a binary High input and is low in frequency for a binary Low input. The binary 1s and 0s are called Mark and Space frequencies.

## Instructions
They are the same as the previous schemes except some changes:
- FSK modulator and demodulator blocks
- Double click on Random integer generator ,change **M-ary number** to 8.

## Scatter plot
### Before Noise
![FSKB](https://github.com/marynader6/commProject-Spring2019/blob/master/FSKB.png)
### After Noise
![FSKA](https://github.com/marynader6/commProject-Spring2019/blob/master/FSKA.png)

## BER performance figure
![FSK](https://github.com/marynader6/commProject-Spring2019/blob/master/FSK.png)


# QAM(16-64) Modulation scheme
## Explanation
Quadrature amplitude modulation (QAM) is the name of a family of digital modulation methods.It conveys two digital bit streams, by changing (modulating) the amplitudes of two carrier waves, using the amplitude-shift keying (ASK) digital modulation scheme or amplitude modulation (AM) analog modulation scheme. The two carrier waves of the same frequency are out of phase with each other by 90°, a condition known as orthogonality and as quadrature.  Since in digital telecommunications the data is usually binary, the number of points in the grid is usually a power of 2 (2, 4, 8, …). Since QAM is usually square, some of these are rare—the most common forms are 16-QAM, 64-QAM and 256-QAM. By moving to a higher-order constellation, it is possible to transmit more bits per symbol. 

## Instructions
They are the same as the previous schemes except some changes:
- QAM modulator and demodulator blocks
- Double click on Random integer generator ,change **M-ary number** to 16 in case of QAM16 and 64 in case of QAM64.

## Scatter plot
### QAM16 Before Noise
![QAM16B](https://github.com/marynader6/commProject-Spring2019/blob/master/QAM16B.png)
### QAM16 After Noise
![QAM16A](https://github.com/marynader6/commProject-Spring2019/blob/master/QAM16A.png)
### QAM64 Before Noise
![QAM64B](https://github.com/marynader6/commProject-Spring2019/blob/master/QAM64B.png)
### QAM64 After Noise
![QAM64A](https://github.com/marynader6/commProject-Spring2019/blob/master/QAM64A.png)

## BER performance figure
### QAM16
![QAM16](https://github.com/marynader6/commProject-Spring2019/blob/master/QAM.png)
### QAM64
![QAM64](https://github.com/marynader6/commProject-Spring2019/blob/master/QAMe.png)
