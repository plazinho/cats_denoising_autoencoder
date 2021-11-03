# Denoising Autoencoder using PyTorch
- Only cats pictures from [Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data) dataset were used for denoising because why not (^._.^)
- All pictures were resized to __128x128__ and normalized in range __[-1, 1]__
- Gaussian noise with a __mean=0__ and __variance=0.08__ was applied to the images
- __10000__ pictures were used for training and __2500__ for testing
- Total parameters of autoencoder: __776,579__
- The training was done for __50__ epochs
- Learning rate scheduler was used to reduce learning rate while training
- Autoencoder architecture:
  
  __Input__
  > ___Images with a shape [3, 128, 128] ->___
  
  __Encoder__
  > ___-> 4 blocks of [Conv2d -> LeakyReLU activation] ->___
   
  __Latent space__
  > ___-> MaxPool2d -> MaxUnpool2d ->___
  
  __Decoder__
  > -> ___4 blocks of [ConvTranspose2d -> LeakyReLU activation] ->___

  __Output__
  > ___-> Tanh activation -> denoised images with a shape [3, 128, 128]___


### Denoising on the 1st epoch 


### Denoising on the 25th epoch 


### Denoising on the 50th epoch 

