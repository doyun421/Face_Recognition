![image](https://github.com/doyun421/Face_Recognition/assets/73266189/6bfd0fb2-7ee5-4aab-8824-542e2a8a3b1c)# Face Recognition

## Face Recognition Use Cases
1) Health Care
     
  - Facial recognition can also be used to diagnose medical disorders in patients with mild or difficult-to-detect symptoms. (e.g., fever, cough, sore throat, malaise by extract patients' expression, feeling of discomfort and lack of well-being, muscle pain, nausea, vomiting, diarrhea, loss of taste and smell)
    e.g. fever: checking thermal infrared camera, cough: frown face, sore throat: holding patient's neck, etc.
    

2) Banking and Finance
- Customer identification and verification can be done through facial recognition.
- Similarly, facial recognition technology can make the customer onboarding process faster.(teaching new customers the value of product or service, keep in their mind their good memory on products by fastly passing onboarding process.)
  
- To reduce ATM robbies or banking fraud cases, facial recognition can be used to add another layer of security. after fingerprint recognition or bio recognition via vein recognition system.

3) Law enforcement and security services
   - Facial recognition has been widely used by law enforcement officers for a while now. It is mainly used to identify and record criminals or persons of interest.
   - Facial recognition is also deployed in various surveillance cameras throughout a city, such as at junctions,
  
     
4)  Entertainment on phone ios security

## Face recognition Skills
1) PyPI -
          using dlib's state-of-the-art face recognition
          The model has an accuracy of 99.8% on Labeled Faces in the Wild 
LFW (Labeled Faces in the Wild) is a public benchmark for face verification, also known as pair matching. (combining two similar things as one group)

- Face verification and other forms of face recognition are very different problems. For example, it is very difficult to extrapolate from performance on verification to performance on 1:N recongition. 

- Many groups are not well represented in LFW. For example, there are very few children, no babies, very few people over the age of 80, and a relatively small proportion of women. In addition, many ethnicities have very minor representation or none at all.


step 1. Find all the faces that appear in a picture

### import face-recognition
python 3.3+

pip3 install face_recognition

installing on raspberry Pi 2/3 with 8GB memory card. 
Write it to a memory card using Etcher (burning the OS image onto removable external media) put the memory card in the RPI and boot it up

for run python3 and type import dlib.
1. Clone the code from github (dlib)
2. Build the main dlib library
3. Build and istal the Python extensions








##index+

dlib C++ library
Dlib is a modern C++ toolkit containing machine learning algorithms and tools for creating complex software in C++. http://dlib.net/

Major Features
- Documentation
     - providing precise documentation for every class and function.
- High Quality Portable code
       The ratio of unit test lines of code to library lines of code is about 1 to 4.
- Machine Learning Algorithms
       Deep Learning
       Conventional SMO(Sequential minimal optimization is an algorithm for solving the quadratic programming problem that arises during the training of suppor-vector machines) based Support Vector

Machines for classification and regression.
 1. Deep Learning input (input layer, hidden layers, output layer) output
 2. Conventional SMO
 3.         


### Face Detection
- Find faces in a photograph
- Find faces in a photograph (using deep learning-cnn)
                                1) Load the jpg file into a numpy array
                                2) Find all the faces in the image using a pre-trained convolutional neural network(face_location function)
                                3) face_location: Returns an array of bounding boxes of human faces in a image
                                   param img = An image (as a numpy array)
                                   param number_of_times_to_upsample: How many times to upsample(Upsampling is the method of putting zero-valued samples between actual samples to increase the sampling rate.) the image looking for faces ![image](https://github.com/doyun421/Face_Recognition/assets/73266189/c554606e-e235-4cba-b083-be46c83817d8) Higher numbers find smaller faces.
                                   param model: Which face detection model to use. "hog" is less accurate but faster on CPUs. "cnn" is a more accurate.
                                    
- Find faces in batches of images w/GPU (using deep learning)
                                1) This finds all faces in a list of images using the CNN model.
                                2) when you need to find faces in LOTS of images very quickly and all the images are the exact same size. This is common in video processing applications where you have lots of video frames to process. 


# Facial Recognition
## 1. Find and recognize unknown faces in a photograph based on photographs of known people
                                a) Load the jpg file into numpy arrays
                                b) Get the face encodings for each face in each image file
                                c) results is an array of True/False telling if the unknown face matched anyone in the known_faces_array
                                d) compare_faces - Compare a list of face encodings against a candidate encoding to see if they match.
                                   param tolerance: how much distance between faces to consider it a match.
## 2.  Compare faces by numeric face distance instead of only True/False matches.
                                a) Often instead of just checking if two faces match or not (True or False), it's heplful to see how similar they are. 
                                1. Load some images to compare against
                                2. Get the face encodings for the known images
                                3. Load a test image anad get encodings for it
                                4. See how far apart the test image is from the known faces
                                * enumerate: 열거하다. 
                                5. distance: np.linalg.norm
                                     norm: Euclidean norm 거리
                                
  
  
