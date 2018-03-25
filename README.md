# Highlight-Detection-in-Sports-Videos-using-Audience-Reaction

Highlights in a sports video are the key exciting moments in the match which attract attention of the spectators in the match. A considerable amount effort is spent in extracting such highlights from the match requiring a lot of investment in terms of time and cost where the domain experts decide which frames must be included in the highlight, thus making it an expensive process, so there should be ways of generating automated highlights. 
We use audience reactions to classify frames in the game as ”highlights” and ”standard play”, because this method can be generalized to detect highlights in any sport. For this purpose, we have used the S-HOCK dataset which contains videos of spectators watching an ice-hockey match.

# <bold>Network Architecture</bold>

The network takes as input video cuboids of 256x256x30, where the first two numbers refer to the spatial dimension while the third is the temporal depth (number of frames). The first
two convolutional layers are composed 16 filters 3x3x3, to
capture spatio-temporal features from the raw data. These
are followed by a 2x2x2 max pooling layer to detect features
at different scales. In the latter two convolutional layers, 10
3x3x3 convolutional filters have been used. In all convolutional
layers the ReLU activation has been used. The network
is then unfolded with a flatten layer followed by three
fully connected layers of decreasing dimensionality (200,
80, and 2 neurons respectively). The final classification task
is achieved by a softmax layer that outputs the probability
of a test sample to belong to each of the two classes: ”highlight”
and ”standard play”. The activation used for the convolution
layer was ReLU and a dropout of 0.5 was added.

YouTube Link: https://www.youtube.com/watch?v=y4Wt10KcIe8&feature=youtu.be
