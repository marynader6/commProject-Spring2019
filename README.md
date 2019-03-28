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
  - 2* Constellation diagram (scatter plot) 
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
