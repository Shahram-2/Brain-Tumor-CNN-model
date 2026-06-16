TensorFlow version: 2.19.0 
 
Training set

glioma images: 501 
pituitary images: 501 
notumor images: 1551 

------------------------ 
Validation set 

glioma images: 150 
pituitary images: 150 
notumor images: 150 

------------------------

Testing set

glioma images: 300 
pituitary images: 300 
notumor images: 301 

------------------------

Total training images: 2553 
Training class proportions: 
glioma  : 0.196 
pituitary: 0.196 
notumor : 0.608 
 
Observation: The dataset is not perfectly balanced, so we will use class weights. 

figure 1: example glioma

<img width="533" height="536" alt="image" src="https://github.com/user-attachments/assets/f96779ef-4401-4d05-aa70-68cc173bd57c" />

------------------------

figure 2: example pituitary

<img width="377" height="381" alt="image" src="https://github.com/user-attachments/assets/d1d2a83f-fc2d-473e-a90e-abb96ccee4e1" />

------------------------

figure 3: no tumor 

<img width="296" height="290" alt="image" src="https://github.com/user-attachments/assets/e5f7ed09-91c9-41ba-a5e7-d59d38c374bf" />


------------------------

Batch size: 32 
Image size: 180 x 180 
Found 2550 files belonging to 3 classes. 
Found 450 files belonging to 3 classes. 
 
Class names: ['glioma', 'notumor', 'pituitary'] 
Number of classes: 3 
Pixel range after normalization: 0.008639706 to 1.0 
 
Class Weights: {0: np.float64(1.7), 1: np.float64(0.5483870967741935), 2: np.float64(1.7)} 

 
Training V1: Baseline CNN 

Epoch 1/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 231s 3s/step - accuracy: 0.7442 - loss: 0.6160 - val_accuracy: 0.7156 - val_loss: 0.6957 
Epoch 2/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 160s 2s/step - accuracy: 0.9741 - loss: 0.0891 - val_accuracy: 0.8289 - val_loss: 0.4535 
Epoch 3/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 159s 2s/step - accuracy: 0.9764 - loss: 0.0698 - val_accuracy: 0.7067 - val_loss: 1.2382 
Epoch 4/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 163s 2s/step - accuracy: 0.9966 - loss: 0.0096 - val_accuracy: 0.8978 - val_loss: 0.3345 
Epoch 5/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 198s 2s/step - accuracy: 0.9897 - loss: 0.0235 - val_accuracy: 0.7911 - val_loss: 0.7955 
Epoch 6/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 159s 2s/step - accuracy: 0.9961 - loss: 0.0117 - val_accuracy: 0.8111 - val_loss: 0.5549 
Epoch 7/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 158s 2s/step - accuracy: 1.0000 - loss: 0.0029 - val_accuracy: 0.7844 - val_loss: 1.0872 
Epoch 8/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 159s 2s/step - accuracy: 1.0000 - loss: 2.9956e-04 - val_accuracy: 0.8111 - val_loss: 0.8184 
Epoch 9/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 158s 2s/step - accuracy: 1.0000 - loss: 1.8652e-04 - val_accuracy: 0.8089 - val_loss: 0.8722 
Epoch 10/10 
80/80 ━━━━━━━━━━━━━━━━━━━━ 158s 2s/step - accuracy: 1.0000 - loss: 9.6300e-05 - val_accuracy: 0.8089 - val_loss: 0.9139 
 

Training V2: CNN + Dropout 

Epoch 1/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 173s 2s/step - accuracy: 0.6569 - loss: 0.8115 - val_accuracy: 0.7733 - val_loss: 0.4883 
Epoch 2/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 201s 2s/step - accuracy: 0.9375 - loss: 0.1921 - val_accuracy: 0.8289 - val_loss: 0.3752 
Epoch 3/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 170s 2s/step - accuracy: 0.9542 - loss: 0.1537 - val_accuracy: 0.7756 - val_loss: 0.5333 
Epoch 4/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 170s 2s/step - accuracy: 0.9730 - loss: 0.0793 - val_accuracy: 0.8378 - val_loss: 0.3978 
Epoch 5/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 171s 2s/step - accuracy: 0.9809 - loss: 0.0692 - val_accuracy: 0.8600 - val_loss: 0.3017 
Epoch 6/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 171s 2s/step - accuracy: 0.9843 - loss: 0.0462 - val_accuracy: 0.7333 - val_loss: 0.8441 
Epoch 7/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 172s 2s/step - accuracy: 0.9865 - loss: 0.0499 - val_accuracy: 0.7822 - val_loss: 0.7445 
Epoch 8/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 171s 2s/step - accuracy: 0.9915 - loss: 0.0318 - val_accuracy: 0.8489 - val_loss: 0.4034 
Epoch 9/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 170s 2s/step - accuracy: 0.9924 - loss: 0.0173 - val_accuracy: 0.7822 - val_loss: 0.9012 
Epoch 10/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 167s 2s/step - accuracy: 0.9951 - loss: 0.0179 - val_accuracy: 0.7511 - val_loss: 1.2597 
Epoch 11/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 167s 2s/step - accuracy: 0.9916 - loss: 0.0259 - val_accuracy: 0.8044 - val_loss: 0.9305 
Epoch 12/12 
80/80 ━━━━━━━━━━━━━━━━━━━━ 201s 2s/step - accuracy: 0.9890 - loss: 0.0275 - val_accuracy: 0.7000 - val_loss: 1.0480 
 

Training V3: Deeper CNN + Augmentation 

Epoch 1/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 248s 3s/step - accuracy: 0.6189 - loss: 0.8977 - val_accuracy: 0.7711 - val_loss: 0.4878 
Epoch 2/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 261s 3s/step - accuracy: 0.8673 - loss: 0.3615 - val_accuracy: 0.9133 - val_loss: 0.2162 
Epoch 3/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 260s 3s/step - accuracy: 0.9113 - loss: 0.2586 - val_accuracy: 0.8733 - val_loss: 0.3438 
Epoch 4/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 244s 3s/step - accuracy: 0.9071 - loss: 0.2608 - val_accuracy: 0.9022 - val_loss: 0.2544 
Epoch 5/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 244s 3s/step - accuracy: 0.9133 - loss: 0.2410 - val_accuracy: 0.9489 - val_loss: 0.1431 
Epoch 6/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 243s 3s/step - accuracy: 0.9432 - loss: 0.1769 - val_accuracy: 0.9533 - val_loss: 0.1378 
Epoch 7/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 243s 3s/step - accuracy: 0.9366 - loss: 0.1720 - val_accuracy: 0.9267 - val_loss: 0.1789 
Epoch 8/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 263s 3s/step - accuracy: 0.9280 - loss: 0.1984 - val_accuracy: 0.9444 - val_loss: 0.1814 
Epoch 9/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 261s 3s/step - accuracy: 0.9582 - loss: 0.1444 - val_accuracy: 0.9511 - val_loss: 0.1349 
Epoch 10/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 315s 4s/step - accuracy: 0.9474 - loss: 0.1337 - val_accuracy: 0.9489 - val_loss: 0.1534 
Epoch 11/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 254s 3s/step - accuracy: 0.9649 - loss: 0.1103 - val_accuracy: 0.8844 - val_loss: 0.3296 
Epoch 12/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 262s 3s/step - accuracy: 0.9687 - loss: 0.1019 - val_accuracy: 0.9356 - val_loss: 0.1864 
Epoch 13/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 254s 3s/step - accuracy: 0.9579 - loss: 0.1531 - val_accuracy: 0.9689 - val_loss: 0.1147 
Epoch 14/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 253s 3s/step - accuracy: 0.9652 - loss: 0.1063 - val_accuracy: 0.9333 - val_loss: 0.1777 
Epoch 15/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 253s 3s/step - accuracy: 0.9670 - loss: 0.0881 - val_accuracy: 0.9822 - val_loss: 0.0621 
Epoch 16/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 253s 3s/step - accuracy: 0.9585 - loss: 0.1174 - val_accuracy: 0.9444 - val_loss: 0.1671 
Epoch 17/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 261s 3s/step - accuracy: 0.9716 - loss: 0.0859 - val_accuracy: 0.9444 - val_loss: 0.1547 
Epoch 18/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 245s 3s/step - accuracy: 0.9762 - loss: 0.0643 - val_accuracy: 0.9756 - val_loss: 0.0872 
Epoch 19/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 243s 3s/step - accuracy: 0.9844 - loss: 0.0457 - val_accuracy: 0.9667 - val_loss: 0.1057 
Epoch 20/20 
80/80 ━━━━━━━━━━━━━━━━━━━━ 278s 3s/step - accuracy: 0.9727 - loss: 0.0819 - val_accuracy: 0.9711 - val_loss: 0.0867 

 
<img width="627" height="216" alt="image" src="https://github.com/user-attachments/assets/6d9a839b-7689-4f2b-8c13-1843bab22c19" />

 <img width="630" height="231" alt="image" src="https://github.com/user-attachments/assets/15b2b694-6422-461b-9a66-5480bcc90cbf" />


Found 900 files belonging to 3 classes. 
 
Evaluating V1 on test set: 
29/29 ━━━━━━━━━━━━━━━━━━━━ 89s 3s/step - accuracy: 0.9233 - loss: 0.5502 
V1 Test Loss: 0.6134068369865417 V1 Test Accuracy: 0.8933333158493042 
 
Evaluating V2 on test set: 
29/29 ━━━━━━━━━━━━━━━━━━━━ 19s 636ms/step - accuracy: 0.8833 - loss: 0.5036 
V2 Test Loss: 0.6055892109870911 V2 Test Accuracy: 0.8433333039283752 
 
Evaluating V3 on test set (final model): 
29/29 ━━━━━━━━━━━━━━━━━━━━ 24s 834ms/step - accuracy: 0.9353 - loss: 0.1749 
V3 Test Loss: 0.17687080800533295 V3 Test Accuracy: 0.9411110877990723 

 
Classification Report (Final Model - V3): 
              precision    recall  f1-score   support 
 
      glioma       0.95      0.90      0.92       300 
    no tumor       0.96      0.99      0.97       300 
   pituitary       0.92      0.94      0.93       300 
 
    accuracy                           0.94       900 
   macro avg       0.94      0.94      0.94       900 
weighted avg       0.94      0.94      0.94       900 

 
 <img width="591" height="496" alt="image" src="https://github.com/user-attachments/assets/786d0187-2ec0-4dba-9cfb-23f0c500bacb" />


 

 

 
