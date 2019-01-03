# Self Supervised Learning
a prominent paradigm is the so-called self-supervised learning that defines an annotation free pretext task,
using only the visual information present on the images or videos, in order to provide a surrogate
supervision signal for feature learning.

The rationale behind such self-supervised tasks is that solving them will force the ConvNet to learn se-
mantic image features that can be useful for other vision tasks.

## Category
### Images
1) [Context](#Context)
2) [Multi-task](#Multi-task)
3) [Image-inpaiting](#Image-inpaiting)
4) [Colorization](#Colorization)
### Video
1) Learning from Temporal Ordering
2) Learning and Using the Arrow of Time
3) Generating Videos with Scene Dynamics

### Invariance
1) Learning by counting
2) Learning by Rotating
3) Transitive invariance
-----
### Context
-----------
#### pros: 
Patch based methods have the advantage of being easy to
understand, network architecture agnostic, and frequently
straightforward to implement. They also tend to perform
well on standard measures of transfer learning.

#### cons: 
1) patch/context-based networks typically suffer
from an issue of being able to “cheat” and bypass learning
the desired semantic structure by finding incidental clues that reveal the location of a patch. Eg: chromatic aberration

2) An often-cited worry in all patch/context works relates
to trivial low-level boundary pattern completion. The neural network may learn the alignment of
patches not based on (for instance) desirable semantic in-
formation, but instead by matching the top or bottom part
of simple line segments. Two common approaches are to
provide a large enough gap between patches and to ran-
domly jitter the patches.

3) In another possible problem for self-supervised networks
in general, mid-layers in the network may not train as well
as the early and later layers.


#### Unsupervised Learning of Visual Representations by Solving Jigsaw Puzzles
* solve Jigsaw puzzles as a pretext task, which requires no manual labeling, and then later repurposed to solve object classification and detection

### Multi-task
-----------
#### Multi-task Self-Supervised Visual Learning
* 1) First, we provide an apples-to-
apples comparison of four different self-supervised tasks
using the very deep ResNet-101 architecture. We then com-
bine tasks to jointly train a network. 2) We also explore **lasso
regularization** to encourage the network to factorize the
information in its representation, and 3) methods for **“har-
monizing” network inputs** in order to learn a more uni-
fied representation.
2) Hightlight: Multi-task scheme; Design a mechanism that allows network to choose which layers are fed into each task
![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202019-01-03%2012-45-00.png)

3) Drawbacks: Not learning tasks simultaneously, the tasks are too different. Pre-preocessing on input data and design of output objective function is needed. 

#### Cross-Domain Self-supervised Multi-task Feature Learning using Synthetic Imagery
*  Given an input synthetic RGB image, our network simultaneously predicts its surface normal, depth, and instance contour, while also minimizing the feature space domain differences between real and synthetic data. 
* Drawbacks: Result no so good or not prominent;  Synthetic image also require human label but with cheap expense. It's hard to categorify into self-supervised framework. 

### Image-inpaiting
-----
#### Self-Supervised Feature Learning by Learning to Spot Artifacts
1) a novel feature learning framework based on detecting images with artifacts, which does not require human annotation; 

2) a method to create images with non-trivial artifacts; * To generate artifacts we first train an autoencoder to reproduce images. * Then, we randomly drop entries from theTo generate artifacts we first train an autoencoder to reproduce images. Then, we randomly drop entries from the encoded feature (at the bottleneck) so that some information about the input image is lost. We then add a repair neural network to the decoder to help it render a realistic image. The repair network inpaints the feature representations at every layer of the decoder, but its limited capacity does not allow it to fully recover the missing information.

3) Hightlight: reproduce damage image through AE, and using Adversarial Learning to distinguish real or fake, and transfer representation in disciminator for other evaluation tasks.

4) Drawbacks: artifact creation need to be further considerated rather mask out some region in encoder feature space.
