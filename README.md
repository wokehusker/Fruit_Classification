# Apples and Plums and Tomatoes! Oh My!
Image classification technologies can be used to address the need for a more efficient grocery shopping experience. This preliminary model hits with 90% accuracy and can be scaled to include all kinds of products.

## Overview 
The grocery industry has its roots in customer service. As such, grocers are always looking for new ways to improve the shopping experience. According to a 2022  McKinsey market analysis, "Loyalty and personalization are more important than ever. Grocers are improving their share of wallet with omnichannel shoppers by expanding their capabilities in personalized promotions and product recommendations." ([McKinsey, The State of Grocery in North America](https://www.mckinsey.com/industries/retail/our-insights/the-state-of-grocery-in-north-america-2022)). In response to this trend, the "Apples and Plums and Tomatoes! Oh My!" project applies image classification technology to correctly identify different types of produce. Images of apples, plums, and tomatoes were chosen as the inputs for this model because of their similar characteristics (red color pallet, smooth exterior, and stem) to make the classification more difficult. Using a dataset of 6915 fruit images from [Kaggle](https://www.kaggle.com/datasets/chrisfilo/fruit-recognition), split into train, validate, and test sets along 80:10:10 lines, the model was able to predict the type of produce with ~90% accuracy. This technology directly addresses the needs discussed above. It has the potential to streamline the shopping experience by automatically adding a charge to the customer's tab when an item is placed in the basket, effectivly eliminating the need for them to wait in a checkout line, and allows grocerers to better tailor their offerings to their patrons. Upon implementation, grocery stores will be able to track what customers buy most often, personalize coupon campaigns to the individual, and suggest other products that might pair well with what is currently in the cart. Image classfication technology could be a massive disruptor in the grocery industry.


![alt text](https://storage.googleapis.com/kagglesdsdata/datasets/500992/928052/Apple/Apple%20B/89red%20applee0064689.png?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20230407%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20230407T052915Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=29c5d815de2cb5baf3356773a38493aad3d44ff7a5badad4d9f6bde9593cbf566c8c77654ed601f7bea108bcbe87248d81368a755ac5b7f61b1a3c6e58081dd795fd8077abe6314b8567ea247183cc88dac2f38c8ff957a595501aab9413190bf6e298fef43906ce5cbe419b0464d16c70cca7033dde7c847c8350d591e5ea864066a7a158a4811c7ad9ddb528252803b510a6c26ed0d4b61d5b8fed61ffe0c9ee96aca3f1ba20f75c4fe90d5a9f5b36236ee40e2c5956db0dda66437f2b4bc713a5a8d191dfc7fcadc860cb8d641c3dfa417e7409f85fc55813311861ea63626072bf6261851ee5d9b657eac4589544c5e96e150224b6b8008f1cb4fee74f3e)     ![alt text](https://storage.googleapis.com/kagglesdsdata/datasets/500992/928052/Tomatoes/Tamotoes00100.png?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20230407%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20230407T050335Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=47854775313c53eedf7f520da59c6f96dde5866d0e30bc0a8c33f411bc90aad907cd085e040802797731785607d2481bc73fac089827e56957261c3ecc3857111a69e5b699a2ba2613401deef5dc4f286cea7b237553ef0bb346372d1d16b586d636a7ad52783cdc8571563f82968eba2a5a07cf4a4e9e3a8c639cb27599e8831237dceb05e200be47491b7c77d798d296818cd5f3b353592cfc3038ff61973ba2335041218bc9cc64685352db2aa56df5e9c7c526eb38d58914eae2050461b3f8222179c0a82fb65fec15a9584ee1e0a0b80a19cfbb53081bd60fe21da3ac2eba951c7c872829de4d1ffd26a47969a46dd4e68fcffc173fe1f15aeaf4c9a5bd)


## Data Science Steps
* Download images from Kaggle using link above
* Delete folders named "Apples D", "Apples E", "Apples F", and "Total Number of Apples"
* Access the contents of the respective raw image data folders
* Create a Pandas DataFrame to hold image IDs and correct classification
* Create directories for our train, validate, and test sets with subdirectories for apples, plums, and tomatoes
* Split the images into train, validate, and test sets
* Initialize base model using a pre-trained CNN (VGG19)
* Define model architecture using 'relu' and 'softmax' activation functions and freeze the model
* Resize and normalize the images
* Train the model on 5 epochs of 10 steps and batch size 50
* Evaluate the model using the test set

## Key Takeaways
* The grocery industry is starved for ways of more efficiently and more personally serving their customers.
* Convolutional Neural Networks (CNNs) have the ability to distinguish between objects with similar characteristics, with a high degree of accuracy.
* The model showcased herein classifies apples, plums, and tomatoes with roughly 90% accuracy.
* This technology can be integrated into shopping carts to improve the shopping experience and drive value for grocery stores.

## Repository Navigation
* You can find the code for the model in the Jupyter Notebook labeled "Apples and Plums and Tomatoes! Oh My!". 
* The folders containing the raw images can be found in the .gitignore. This was done to avoid difficulties uploading the multple GB worth of image data to GitHub. 
* The folder titled "images" contains images for this ReadME.
* PDF copies of both the Jupyter Notebook and the Final Presentation are also included
