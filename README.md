# BPSK Modulation scheme
## Explanation
        Binary Phase Shift Keying (BPSK) is a type of digital modulation technique in which we are sending one bit per symbol i.e., ‘0’ or a ‘1.It is a two phase modulation scheme, where the 0’s and 1’s in a binary message are represented by two different phase states in the carrier signal: θ=0∘ for binary 1 and θ=180∘ for binary 0.
        s1(t)=Ac cos(2πfct),0≤t≤Tb for binary 1
        s0(t)=Ac cos(2πfct+π),0≤t≤Tb for binary 0
        


## Instructions
* To get blocks click on the model (white sketch ) and write name of the block you want.
        * Double click on Random integer generator ,change *M-ary number* to 2.
        * Double click on error rate calculation block and in *output data* choose port instead of workspace,so you can connect the                 Display block.
        * Double click on To workspace block change *limit data points to last* to 2, then *save format* to array,
          then *save 2-D signals as* choose 2-D array.
