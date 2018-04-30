# Local-Binary-Pattern-training

The license plate region detector uses the Local Binary Pattern (LBP) algorithm
Easy way to HaarCascade Training in python.

Edit the prep.py script and change the WIDTH, HEIGHT, and COUNTRY variables to match the country that you are training.  The width and height should be proportional to the plate size.  A total pixel area of around 650 seems to work best.  Also, adjust the path to your OpenCV libraries, if that needs to be changed.

Once you are ready to start training, enter the following commands:

  - rm ./out/*    (clear the out folder in case it has data from previous runs)
  - ./prep.py neg
  - ./prep.py pos
  - ./prep.py train

# Requirment.
Python 2.7, 
Numpy, 
opencv

# Command-run
opencv_traincascade -data ./out/ -vec ./positive/vecfile.vec -bg ./negative/negative.txt -w 120 -h 60 -numPos 99 -numNeg 5  -featureType LBP -numStages 20
