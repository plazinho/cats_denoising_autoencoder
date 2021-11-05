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

## Some denoised images. More of them you can find [here](https://github.com/plazinho/cats_denoising_autoencoder/tree/main/more%20images)

![clear-noised-1-10-50-16images-final](https://user-images.githubusercontent.com/88561819/140078530-bcf4e8d0-e09d-419c-9b71-ba31b949c926.png)

![clear-noised-1-10-50-8images-final](https://user-images.githubusercontent.com/88561819/140079161-b7533772-ae21-4d37-b693-23abb9fbd87f.png)
