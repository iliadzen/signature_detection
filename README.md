# signature_detection
## Summary
Model for determining the presence of a signature on a fragment of a document. This fragment can be found near common words (such as *Sincerely, Yours* and etc.), whose position can determined by OCR methods (open source Tesseract for example).
## Dataset
To train model Tobacco 800 dataset was used: http://tc11.cvc.uab.es/datasets/Tobacco800_1


The dataset contains documents in tif format with marked signatures positions in XML files.
Extracting signatures (class 1) fragments and sampling fragments without signatures (class 0) are in *data_preparation.ipynb*.


## Model description

## Accuracy
## Usage
Pretrained model is *model_v1.h5*  
Input image shape: (150, 150, 3)
1) Load model:  
model = keras.models.load_model('path_to_model/model_v1.h5')
2) Load image:   
img = Image.open('path_to_image')
3) Resize image:  
img = img.resize((150, 150), Image.ANTIALIAS)  
img = np.expand_dims(np.asarray(img), axis=0)
4) Make prediction (returns probability):  
model.predict(img)[0][0]

