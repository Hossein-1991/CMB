# investigation-of-the-non-Gaussianity-in-the-simulated-CMB-using-convolutional-neural-networks

Non-Gaussianity:
-----------------
Several models of the inflation predict a roughly perfect Gaussian primordial fluctutations which are generated by a single scalar quantum field in ground state. This is while there are alternative approaches to decribe the inflationary period which lead to the non-Gaussianity of the CMB.

From this point of view, detecting non-Gaussian patterns in the CMB radiation plays a crucial role in confining cosmological models.

Research goal:
---------------------
My primary aim in this research is to design a network which is able to indentify footprint of primordial non-Gaussianity in the simulated data fluctuations. 

Data source:
-------------
I used simulated data that are available here:
http://dc.zah.uni-heidelberg.de/elsnersim/q/s/fixed

A succinct description of research results:
---------------------------------------------
According to the mathematical background, I considered three different amounts of f_NL and, therefore, my data set has three classes.

The utilized CNN is called Resnet18 that has 18 layers. Although the predefined input channel of mentioned network is 3, I altered it to 1 channel (it is possible to merge images using ```np.repeat``` to create a 3 channel input, but due to lack of free space on my drive, I preferred 1 channel case. The output of network will not change dramatically)

To prevent overfitting, I employed the cross-validation technique. As a result, the network reached a maximum of about 99% on validation accuracy.  
