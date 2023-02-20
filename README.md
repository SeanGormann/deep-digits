# deep-digits
Exploring the use of MLP's and CNN's to classify handwritten digits with PyTorch. 

18/02/23
Updated the repo with files for the MLP. It was fun to put this into action after learning a substantial amount about the theory behind ANN's. After loading the data and preparing it appropriately, a relatively small MLP was constructed with 110,000 parameters. The data was batched and fed to the network with the loss being calculated and model being optimised with the ADAM optimizer over an undoubtebly small 10 epochs. 

Loss:
![loss-over-time](https://user-images.githubusercontent.com/100109163/219882812-630d2dc6-c403-4355-a088-2341cde71aaa.png)


The model was then evaluated on the test set and accuracy was recorded. Even with the small size and train time, the model still achieved an accuracy of approximately 95%.

19/02/23
Updated the repo with an implementation of a CNN. It was quite interesting to see how the abstraction of features through kernel filters impacted the learning process. The training was seemingly immediately improved and converged to an extremely high accuracy (99.5%!) after the same 10 epochs as the MLP. That being said the model had 10x the amount of parameters and took much longer to train. I also implemented methods to save the model and record it's accuracy in a more automated and efficient way. 

Loss:
![CNN-loss-over-time](https://user-images.githubusercontent.com/100109163/220102930-79ce8d58-a24f-4398-a776-603c657d2d62.png)


Overall & class by class performance:

{
  "overall": {
    "precision": 0.998684516831351,
    "recall": 0.9986833333333334,
    "f1": 0.9986832272223732,
    "num_samples": 60000.0
  },
  "class": {
    "0": {
      "precision": 0.999662276258021,
      "recall": 0.9994934999155833,
      "f1": 0.9995778809624314,
      "num_samples": 5923.0
    },
    "1": {
      "precision": 0.9974848350347685,
      "recall": 1.0,
      "f1": 0.9987408340122954,
      "num_samples": 6742.0
    },
    "2": {
      "precision": 0.9996634129922585,
      "recall": 0.9969788519637462,
      "f1": 0.9983193277310923,
      "num_samples": 5958.0
    },
    "3": {
      "precision": 0.9996736292428199,
      "recall": 0.9991844723536127,
      "f1": 0.9994289909454278,
      "num_samples": 6131.0
    },
    "4": {
      "precision": 0.9976064284493076,
      "recall": 0.9988017802122561,
      "f1": 0.9982037464716448,
      "num_samples": 5842.0
    },
    "5": {
      "precision": 0.9998152254249815,
      "recall": 0.998155321896329,
      "f1": 0.9989845841410504,
      "num_samples": 5421.0
    },
    "6": {
      "precision": 0.9988171679621494,
      "recall": 0.9988171679621494,
      "f1": 0.9988171679621494,
      "num_samples": 5918.0
    },
    "7": {
      "precision": 0.9976084183673469,
      "recall": 0.9987230646448524,
      "f1": 0.9981654303262344,
      "num_samples": 6265.0
    },
    "8": {
      "precision": 0.9981235073353805,
      "recall": 1.0,
      "f1": 0.9990608725347905,
      "num_samples": 5851.0
    },
    "9": {
      "precision": 0.9986522911051213,
      "recall": 0.9964699949571356,
      "f1": 0.997559949516197,
      "num_samples": 5949.0
    }
  }
}
