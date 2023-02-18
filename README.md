# deep-digits
Exploring the use of MLP's and CNN's to classify handwritten digits with PyTorch. 

18/02/23
Updated the repo with files for the MLP. It was fun to put this into action after learning a substantial amount about the theory behind ANN's. After loading the data and preparing it appropriately, a relatively small MLP was constructed with 110,000 parameters. The data was batched and fed to the network with the loss being calculated and model being optimised with the ADAM optimizer over an undoubtebly small 10 epochs. 

Loss:

![loss-over-time](https://user-images.githubusercontent.com/100109163/219882812-630d2dc6-c403-4355-a088-2341cde71aaa.png)


The model was then evaluated on the test set and accuracy was recorded. Even with the small size and train time, the model still achieved an accuracy of approximately 95%.
