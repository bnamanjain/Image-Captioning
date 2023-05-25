# Image-Captioning
Here, My goal was to make an AI tool which would use Image-Captioning and give out the caption related to the image. I have used a pre-trained model from HuggingFace.com. Refer read_me for more. Thanks
It uses both Natural Language Processing and Computer Vision to generate the captions.

sample dataset : 

First I went to google/youtube/huggingface.com, where I wanted to know what libraries to be used. On google/YT i got around 2-3 options:
  a. CNN+RNN
  b. CNN+LSTM : https://www.youtube.com/watch?v=fUSTbGrL1tc&t=444s&ab_channel=HackersRealm
  c. Using TRANSFORMERS :https://www.youtube.com/watch?v=8PzcmL9d3zM&ab_channel=AIAnytime

I have trained this dataset for only aroudn 100 images and captions pairs. I should have trained for more. 

So, I spent around 4-5 hours reading about the difference in performance among all of these and I found the respective models as well, which were using CNN/Transformers. CNN have been ruling th space of Computer vision for almost all the time now, but after transformers came in it changed the game entirely, how ? Lets note down some pointers :

 
Steps : 
1. checking what libraires to be used
2. choosing the models - took time
3. choosing dataset 
4. import the transformers model
5. import datasets : I have download the whole dataset from kaggle and uploaded a part of it to the collab, as the original file is too large. 
7. upload images zip 
8. unzip the images files
9. import libraries
10. upload captions csv
11. Make a list of pairs with dictionaries containing the image and caption pairs
12.each dictionary from the captions list is written as a separate line in the file. Each line represents a JSON object (caption) in the JSON Lines format. Inside the with statement, a file object f is created, representing the opened file. The with statement ensures that the file is properly closed after writing, even if an exception occurs. For each item, the json.dumps() function is used to convert the dictionary into a JSON-formatted string.
13. Pytorch Dataloader : Creating a Custom Dataset for your files
14. Preparing your data for training with DataLoaders
15. Iterate through the DataLoader
16. using auto causal model from transformers
17. Instantiating one of the configuration classes of the library from a pre-trained model configuration. - pre_trained
18. optimizer to be used for pytorch, adjusting learning rate
19. We train the model for a total of 20 epochs.


Resources used : 
DATASET: https://www.kaggle.com/datasets/prithvijaunjale/instagram-images-with-captions 
MODEL: https://huggingface.co/docs/transformers/main/en/model_doc/git

1. https://towardsdatascience.com/image-captioning-in-deep-learning-9cd23fb4d8d2
2. https://michael-franke.github.io/npNLG/08-grounded-LMs/08c-NIC-pretrained.html
3. https://github.com/AIAnytime/Image-Caption-Generator-App/blob/main/Notebook%20Code/caption.ipynb
4. https://github.com/hiteshvaidya/Instagram-Caption-Generator
5. https://pytorch.org/docs/stable/data.html - for pytorch documentation
6. https://fairyonice.github.io/Develop_an_image_captioning_deep_learning_model_using_Flickr_8K_data.html
7. https://huggingface.co/transformers/v3.0.2/model_doc/auto.html
8. https://pytorch.org/docs/stable/optim.html
9. https://pytorch.org/docs/stable/optim.html#putting-it-all-together


Things I couldn't complete and would like to work on :
1. Different captions for an image as the dataset contained 1 caption per image. 
Solution suggestion : Might have scraped data using selenium from various other social media sites.
3. The deployment of the model via Streamlit/Docker could be done. 
