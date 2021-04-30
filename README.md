<h3>Aim of the Project</h3>
<p>
Aim of this project is to automatically recognize human actions based onanalysis of the body landmarks using pose estimation.
</p>
<h5>Problem Statement</h5>
<p>
Analysis of people’s actions and activities in public and private environments are highly
necessary for security. This cannot be done manually as the number of cameras for surveillance
produce lengthy hours of video feed every day. Real-time detection and alerting of suspicious
activities or actions are also challenging in these scenarios. This issue can be solved by applying
deep learning-based algorithms for action recognition.
</p>
<h3>Project Description</h3>

<h5>The project has 3 major components:</h5>
<ol>
<li><h6>CNN based Pose Estimation model</h6>
<p>Unpack and load the pre-processed the dataset with images and joint coordinates. Each pose
image contains 7 body joints represented using 14 floating point numbers. Build the CNN
model for the dataset and train for few epochs. Test the model with testing set and do
inference with single data samples. Save the model. Train a transfer learning model with
already trained CNN base model.</p>
</li>

<li><h6>NN based Action Recognition model</h6>
<p>Load the dataset with pose joints as features and actions labels (‘Namaste’ vs ‘Hello’). Split the
dataset into training and testing. Train the model for few epochs, test the model, save the model.
Analyze the model with new samples of data. Based on the results, flip invariant data
augmentation is performed to increase the accuracy where further graph-like features are
extracted from the dataset. Training, testing and inferencing is accomplished with the
augmented graph features of the dataset.
</p>
</li>

<li><h6>Action Recognition in videos</h6>
<p>CNN based pose estimation model and neural networks-based action recognition model is
combined to work on images and videos. Action recognition in videos is achieved by processing
the frames one by one using the model.
</p>
</li>
</ol>
<h4>Dataset Description</h4>
<h6><a href="https://drive.google.com/file/d/1vFqbSbvXR_eF_ltTI0MgWKI2sFbiChsh/view?usp=sharing" target="_blank">Download Dataset: Frames Labeled in Cinema (FLIC)</a></h6>
<p>
The dataset is a collection of 5003 image from popular Hollywood movies. The images were
obtained by running a state-of-the-art person detector on every tenth frame of 30 movies.
People detected with high confidence (roughly 20K candidates) were then sent to the
crowdsourcing marketplace Amazon Mechanical Turk to obtain ground-truth-labeling. Each 
image was annotated by five Turkers for $0.01 each to label 10 upper body joints. The median-
of-five labeling was taken in each image to be robust to outlier annotation. Finally, images were
rejected manually by us if the person was occluded or severely non-frontal. We set aside 20%
(1016 images) of the data for testing.
</p>
