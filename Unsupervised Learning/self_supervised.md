# Self Supervised Learning
a prominent paradigm is the so-called self-supervised learning that defines an annotation free pretext task,
using only the visual information present on the images or videos, in order to provide a surrogate
supervision signal for feature learning.

The rationale behind such self-supervised tasks is that solving them will force the ConvNet to learn se-
mantic image features that can be useful for other vision tasks.

## Category
### Images
1) [Context](#Context)
2) Jigsaw puzzle
3) impaining 
4) Colorization
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


image completion, image colorization, motion segmentation, motion frame ordering, object counting and a multi-task ensemble of many models.

----
## Unsupervised Learning of Visual Representations by Solving Jigsaw Puzzles
* solve Jigsaw puzzles as a pretext task, which requires no manual labeling, and then later repurposed to solve object classification and detection


