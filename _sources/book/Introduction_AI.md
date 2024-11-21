# Introduction to Artificial Intelligence in Marine Science

## Overview
In this section 
***Context for AI in marine science, with a focus on how CV fits within ML and AI more broadly, examples of other marine science problems that use AI, examples of ML that students may have encountered already)

### Learning Objectives
By the end of this section, you will:
- Understand the difference between artificial intelligence terms that are often used interchangeably 
- Identify marine science problems suitable for AI

---

# A non-comprehensive review of AI 
## What is Artificial Intelligence (AI)
Artificial Intelligence (AI) is a broad field with the goal of developing computers and robots that can mimic and go beyond human capabilities. Some examples of these capabilities include recognizing objects or sound, understanding natural language, and solving complex problems. AI is often used interchangeably with the term machine learning (ML) and many AI advancements are underpinned by ML, but ML is one of several subdomains. Examples of other subdomains include deep learning, robotics, neural networks, and natural language processing. These subdomains are not mutually exclusive and can be used in combination with one another or even in some cases be considered subfields of one another. For example deep learning is a subfield of machine learning. 

***Graph of AI, ML, DL subdomain here

## What is Machine Learning (ML)
Machine learning (ML) is a subset of AI where an algorithm or a set of algorithms learn from the environment. Instead of being explicitly programmed for a task, the algorithm or model is able to learn to solve a task by analyzing data, learning from experience, and making inferences. Ideally, ML algorithms improve over time as they are exposed to more data, however the quality of the data and the objective of the model can impact the overall quality even when large quantities of data are available.

***Discuss the math? relatively simple but lots and lots of it

***Include examples of classic ML? Like SVM and decision tree?

```{seealso}
If you are interested in learning more about Machine Learning check out....
```

### Supervised vs Unsupervised Learning
Machine learning can often be divided between supervised and unsupervised approaches. Supervised systems are given input data and their corresponding output (measurements or labels assigned by experts; the "correct" answer). These systems learn and map connections between the input and the output (correct answers) until they are able to apply these connections to unseen data. Unsupervised systems are only given input data and search for patterns, the goal for these systems is to identify meaningful patterns. A common use of unsupervised methods is to cluster data points or conversely identify outliers. 

This course will primarily focus on supervised methods.

### What is Deep Learning and Neural Networks
Deep learning (DL) is a subfield of machine learning. The difference between deep learning and traditional machine learning is the structure of the underlying neural network. Traditional ML models have simple neural networks with one or two computational layers, while DL models have more than the three layers and as many as hundreds of thousands of layers. Neural networks are designed to mimic the human brain. An example of these are convolution neural networks (CNNS) which are primarily used in computer vision and will be the focus of this course. 

Some challenges of deep learning and neural networks is that they need lots of data and computing power. They are also often "black boxes" making them harder to understand and causing issues with transferring between use cases. 


### What is Computer Vision (CV)
Computer vision (CV) is a subfield of machine learning that focuses on machines being able to interpret visual data (images and video), such as identifying and classifying objects.

# Uses of AI in Marine Sciences