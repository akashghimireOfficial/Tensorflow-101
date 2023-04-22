Why is it necessary to build tf pipeleine? I mean it is much easier just to train on numpy dataset. So, why use extra effort? 

==> Before, answering this we need to know what happens when we train data using numpy, then all of the data is loaded in to the memory directly.
> In this scenario what happen if the training dataset is too large and can't fit into a memory? 

So, to handle this scenario tensorflor provides **tf.data** api which can handle large dataset. Using tf.data we can use dataset as iterator thus we don't need to load whole dataset within the memory. Beside handling large training dataset other advantages of using tf.data training pipeline are: 

1. Preprocessing during data. tf.data provides flexible way to preprocess dataset while training. Examples are if you are training images then you can do preprocessing steps such as rotation before training.
2. tf.data provide consistent for working with different data types such as csv,images, video and so on.
3. tf.data can also provide better compatibility with distributed training frameworks such as TensorFlow's tf.distribute API, which can help to scale training across multiple GPUs or machines.


 
 We usually use **tf.data.Dataset** method to handle tf data.  We will learn this in upcoming slides
