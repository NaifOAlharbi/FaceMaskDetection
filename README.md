# FaceMaskDetection
Face mask detector  

The goal of this application is to detect the mask from live-feed camera. It depends on 2 techniques, face detection then classifying the detected face wears a mask or not. It can be called face mask detection.



__1- Face detection:-__
First,we will detect the face from the frame then the face will be extracted as Region Of Interset (ROI). The ROI will be feeded to our next model which will classify if there is mask or not in the extracted (ROI). The face detector model is a deep learning model and it is pre-trained for face detection. This model is one of Caffe models, Caffe is a deep learning framework. It has many other pre-trained models for different purposes (https://github.com/BVLC/caffe/wiki/Model-Zoo). After downloding the face detection model ("deploy.prototxt") and its weights ("res10_300x300_ssd_iter_140000.caffemodel"), it can be applied and loaded to OpenCV library by using (dnn module). 


__2- Mask detection:-__  
After detecting the face, the ROI will be extracted and feed to mask classifier, which will classify if there is a mask or not. In this part we trained our own modle by using the transfer learning, chechk this blog for further information about transfer learning
 (https://www.datacamp.com/community/tutorials/transfer-learning?utm_source=adwords_ppc&utm_campaignid=10267161064&utm_adgroupid=102842301792&utm_device=c&utm_keyword=&utm_matchtype=b&utm_network=g&utm_adpostion=&utm_creative=278443377095&utm_targetid=aud-299261629574:dsa-429603003980&utm_loc_interest_ms=&utm_loc_physical_ms=9076704&gclid=CjwKCAjw57b3BRBlEiwA1ImytlgsNBbAs0yXxWKTfQ5HJXF4gdodFDvInrCESZg8EgOQ1aeqTjBaVxoCQ4oQAvD_BwE)


 The Mobilenetv2 is one of the most famous models. It can be considered as light weight model for image classification, Mobilenetv2  is a significant improvement over MobileNetV1 and pushes the state of the art for mobile visual recognition including classification, object detection and semantic segmentation. We have trained this model by useing TensorFlow, based on the dataset that we obtianed. The dataset is images of face and Mask face.By using the Fine-tuning technique in transfer learning we trained the Mobilenetv2 based one our dataset.  



