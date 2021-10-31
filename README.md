# Denoising Autoencoder using PyTorch
- Only cats pictures from [Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data) dataset were used for denoising because why not (^._.^)
- All pictures were resized to __128x128__
- Gaussian noise was applied to the images (__10000__ pictures were used for training)
- Total parameters for autoencoder: __113,091__
- Encoder architecture:

  ___3 blocks of [Conv2d -> ReLU activation -> BatchNorm2d] -> MaxPool2d___ 
- Decoder architecture:

  ___Upsample -> 2 blocks of [ConvTranspose2d -> ReLU activation -> BatchNorm2d] -> ConvTranspose2d -> Sigmoid activation___
- The training was done for __30__ epochs

### Denoising on the 1st epoch 
![first_epoch](https://user-images.githubusercontent.com/88561819/139597149-c3bd76dc-8704-460d-98ac-8f92a26ea584.jpg)

### Denoising on the 20th epoch 
![20_epoch](https://user-images.githubusercontent.com/88561819/139597174-84c652d1-32ba-46c7-a30e-5b8c1ef398fd.jpg)

### Denoising on the 30th epoch 
![30_epoch](https://user-images.githubusercontent.com/88561819/139597784-72163f51-37b4-45ea-94a6-1c8f9cefa975.jpg)
