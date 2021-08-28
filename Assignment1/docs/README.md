# Assignment Plan
> 07/08/21 - 11/08/21
* Read [Article on MobileNets](https://medium.com/@yu4u/why-mobilenet-and-its-variants-e-g-shufflenet-are-fast-1c7048b9618d) didnt understand much 
* Watched [MIT 6.S191](https://www.youtube.com/watch?v=BUNl0To1IVw&list=RDCMUCtslD4DGH6PKyG_1gFAX7sg&start_radio=1&rv=BUNl0To1IVw&t=2&ab_channel=AlexanderAmini) to brush up CNNs again
* Read [Intro to audio analysis](https://medium.com/behavioral-signals-ai/intro-to-audio-analysis-recognizing-sounds-using-machine-learning-20fd646a0ec5) 
* Read [Audio classification using CNNs](https://medium.com/x8-the-ai-community/audio-classification-using-cnn-coding-example-f9cbd272269e)
* Tried to understand the [code](https://colab.research.google.com/drive/1A46yAHC7uGr-mKggasHbBtodZ6wYZvv1?usp=sharing)
* Still figuring out stuff 

> 12/08/21 - 18/08/21
* Reverted back to original algorithm as my experiments to make the model better kept hitting a dead end
* Finalized the previous algorithm with minor changes (disregarding averaging out of the audio tensors)
* Divided the test based on silence between two consecutive words
* Transformed the generated audio files to extract out mfcc features 
* Generated logits from the CNN after passing the test audio chunks through it 
* No luck so far with the accuracy on the test audio file data (even after reducing noise and removing audio files that were not properly split)
* Possible fixes - 1. Might try stft , lot of padding is involved learning is less i think its because of this

> 19/08/21 - 28/08/21
* Did a lot of experimenting but am unable to narrow down as to what is causing the model to perform badly on real dataset
* Tried training on freespeak dataset to check if there's something wrong with MNIST but even freespeak performed poorly on real dataset
* Introduced strides on 2 more layers to reduce overfitting and saw some improvement from the model
* Reduced number of epochs and further saw improvements
* Added dropout layer only to check overfitting and the model 
* Motive now is to make the model work better on audios that are not very similar to the MNIST data
* Tried Regularization and it worked , the problem detected was correct 
* Significantly reduced the computational complexity of the model , its lighter and faster now
* A lot of improvements can be still be made just by adjusting the parameters of regularizer
* Read [Artcle on Regularization](https://towardsdatascience.com/types-of-regularization-in-machine-learning-eb5ce5f9bf50) 
* Read [another article for the same](https://towardsdatascience.com/regularization-in-deep-learning-l1-l2-and-dropout-377e75acc036)
* Read [CS231n Convolutional Neural Networks for Visual Recognition](https://cs231n.github.io/linear-classify/)

