



# Knowledge Distillation
This is a list of recent papers in the field of knowledge distillation. Although there are great repositories in this regard like [awesome-knowledge-distillation](https://github.com/dkozlov/awesome-knowledge-distillation) and [knowledge-distillation-papers
](https://github.com/lhyfst/knowledge-distillation-papers), I am trying to make this one more comprehensive and updated, including summaries of each paper. There could be some mistakes in the details or summaries. Please let me know if you have any suggestions or edits.

- [Questions on knowledge distillation for beginners](questions.md)
- [Looking for the codes?](implementations.md)



--------
## Knowledge Distillation Papers
- (15.03.09, NIPS 2014) [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531)
        

> Proposed knowledge distillation (KD), as we know now, for the first
> time.

    Datasets: MNIST, JFT
    Networks: Manual CNNs with different number of layers

- (17.06.01, CVPR 2018) [Deep Mutual Learning](https://arxiv.org/abs/1706.00384)

> Proposed to train the teacher and the student together iteratively by
> using the other one's soft labels.

    Datasets: CIFAR-100, Market-1501
    Networks: Wide-ResNet, MobilNet, ResNet, Inception

- (18.05.15, AAAI 2019) [Knowledge Distillation with Adversarial Samples Supporting Decision Boundary](https://arxiv.org/abs/1805.05532)
        
> Proposed to generate samples close to the decision boundary of the teacher in that the knowledge of a teacher network would be transferred more effectively by utilizing those samples. 

    Datasets: ImageNet, CIFAR-10, TinyImageNet
    Networks: ResNet
        
- (18.05.29, ICML 2018) [Born Again Neural Networks](https://arxiv.org/abs/1805.04770)
>    Argued that the teacher could have the same size as the student.

    Datasets: CIFAR-10, CIFAR-100, Penn Tree Bank (PTB)
    Networks: ResNet, Wide-ResNet, DenseNet, ConvLSTM, LSTM

- (18.11.08, AAAI 2019) [Knowledge Transfer via Distillation of Activation Boundaries Formed by Hidden Neurons](https://arxiv.org/abs/1811.03233)

>    Proposed an activation transfer loss that minimizes the difference of neuron activations between the teacher and the student. The proposed method concentrates on the activation of neurons, not the magnitude of neuron responses. This concentration enables more precise transfer of the activation boundaries.

    Datasets: CIFAR-10, CUB 2011, MIT scenes
    Networks: Wide-ResNet, ResNet, Mobilenet

- (19.02.09) [Improved Knowledge Distillation via Teacher Assistant](https://arxiv.org/abs/1902.03393)

>    Proposed to use networks with sizes between the teacher and the student to provide less complex soft targets for the student.

    Datasets: CIFAR-10, CIFAR-100
    Networks: ResNet, Plain CNN

- (19.04.10, CVPR 2019) [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068?context=cs.LG)

> Proposed to transfer the structure of the soft targets between several pairs of samples instead of a single soft target.

    Datasets: CUB-200, Cars 196, Stanford Online Products, CIFAR-100, Tiny ImageNet datasets, miniImageNet, Omniglot
    Networks: ResNet, VGG, GoogLeNet


- (19.04.19) [Knowledge Distillation via Route Constrained Optimization](https://arxiv.org/abs/1904.09149)

>    Proposed to also use the intermediate epochs of the teacher instead of just using the final teacher to solve the gap problem.

    Datasets: ImageNet, CIFAR-100, MS- Celeb-1M, IMDb-Face
    Networks: MobileNet, ResNet

## Applications in other tasks

**Metric Learning**:
- (17.07.05, AAAI 2018) [DarkRank: Accelerating Deep Metric Learning via Cross Sample Similarities Transfer](https://arxiv.org/abs/1707.01220)

>  Transfers similarity ranks between data examples instead of the hard labels of similarity and dissimilarity

**Network Compression**: 
- (18.02.15, ICLR 2018) [Model compression via distillation and quantization](https://arxiv.org/abs/1802.05668)

>  Proposed Quantized Distillation which jointly leverages weight quantization and distillation in an iterative manner.

**Object Detection**: 
- (19.01.02) [Learning Efficient Detector with Semi-supervised Adaptive Distillation](https://arxiv.org/abs/1901.00366)

>  Benefits from the teacher's knowledge to focus on the hard-to-learn samples predicted by teacher with low certainty and hard-to-mimic samples with a large gap between the teacher’s and the student’s predictions.

- (NIPS 2017) [Learning Efficient Object Detection Models with Knowledge Distillation](https://papers.nips.cc/paper/6676-learning-efficient-object-detection-models-with-knowledge-distillation.pdf)

> Proposed Knowledge Distillation between different detectors for improving speed and accuracy (different resolutions), and a new loss function to transfer knowledge for the regression parts.

**Super-Resolution**: 
- (18.06.05) [Adaptive Importance Learning for Improving Lightweight Image Super-resolution Network](https://arxiv.org/abs/1806.01576)

>  Proposed an adaptive importance learning scheme based on the Teacher's error for each pixel.

**Incremental Learning**:
- (16.06.29, ECCV 2016) [Learning without Forgetting](https://arxiv.org/abs/1606.09282)

>  Proposed to use the soft targets of the images from the new task and the old model, in addition to the GT labels, to train the new model. By doing so, it decreases the forgetting of the previous tasks.

- (18.11.20, CVPR 2019) [Learning without Memorizing](https://arxiv.org/abs/1811.08051)

>  Proposed to use an attention loss in addition to the KD loss to further improve the transferred knowledge for incremental learning.

- (19.03.29) [Incremental Learning with Unlabeled Data in the Wild](https://arxiv.org/abs/1903.12648)

>  Instead of using the soft targets of the previous model and the GT label of the new task for training the new model, this paper proposed to use the soft targets of the previous model and a new model which is trained on the new task to train a final model.



