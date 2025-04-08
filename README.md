# erc_assignment_sub
The flow of the program is,

I first load the noisy file and plot the time domain signal,
then I perform FFT on it to go to the frequency domain and make a plot of magnitude versus frequency. 
After this I will see the highest peak in the graph which corresponds to the carrier frequency. 
Next we demodulate the signal (multiply with cos2pifct) and plo the demodulated signal. 
Now we are ready to apply the bandpass filter. Using butter of scipy we make a butterworth bandpass filter (ranges i took 100 and 4500 - i started with standard range of 300 - 3400 and then just kept changing until it was clear), 
then I used filtfilt to make it smooth (applies filter twice forward and backward), 
then i tried to make it cleaner by removing some low amplitude noise and some high amplitude noise (logic was if its above or below a certain threshold make that sample/component 0 magnitude otherwise let it be). 
Finally we plot the filtered signal and then download the cleaned audio (need to convert it to int because it cant play in float format so I did normalization/rescaling).
