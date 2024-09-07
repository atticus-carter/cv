# Image Annotation Overview

When training models using imagery data, it is crucial to provide the algorithm with properly annotated training data. This allows the model to learn what to look for and where to find it within an image. Imagine, for a moment, that you are a computer tasked with identifying every rockfish in an image, but the image is completely unannotated, and you have no prior knowledge or context of what a rockfish looks like. You would likely have a (very) hard time piecing together what that request even means. In the context of computer vision, image annotation serves as a vital guide, providing the labels and boundaries necessary for the model to understand its task. Without annotations, the model would be left guessing, unable to differentiate between objects or recognize key features. Image annotation refers to the process of labeling images in a way that helps the machine learning model recognize objects, patterns, or other relevant features. Depending on the specific task at hand, there are different types of annotations that can be applied, each serving a distinct purpose in guiding the model's learning process. For this lesson, we will focus on the most common annotation types, as these are foundational for many computer vision tasks and essential for developing accurate and efficient models. Proper annotation not only improves the model’s ability to detect and classify objects but also ensures the quality and reliability of the outputs in real-world applications. There are various types of annotations depending on the task, but the most common ones we'll focus on in this lesson are:

1. **Bounding Boxes**
2. **Instance Segmentation**
3. **Keypoint Annotation**

These annotation types are essential for different computer vision tasks, such as object detection, segmentation, and pose estimation.

## 1. Bounding Boxes

Bounding boxes are one of the simplest and most widely used types of annotations. They involve drawing a rectangle around an object of interest in the image.

:::{figure} images/poralia.png
:name: bboxes_example
Multiple Organisms are annotated using bounding boxes Credit: A.Carter, OOI-NSF
:::

### Format in PyTorch

In PyTorch, the bounding box format is typically represented as `[x_min, y_min, x_max, y_max]`, where:
- `x_min`, `y_min`: Coordinates of the top-left corner of the box.
- `x_max`, `y_max`: Coordinates of the bottom-right corner of the box.

Example PyTorch annotation for a bounding box:

`'boxes': torch.tensor([[10, 20, 200, 400], [50, 60, 220, 420]]), 'labels': torch.tensor([1, 2])`

Here, two bounding boxes are defined with class labels `1` and `2` respectively.

## 2. Instance Segmentation

Instance segmentation is a more detailed annotation technique where each pixel in the object is labeled. This differs from bounding boxes, which only define the region around an object. With instance segmentation, each object instance has its own mask.

### Format in PyTorch

In PyTorch, instance segmentation masks are represented as binary masks (same size as the image), where each pixel is marked as either belonging to the object (1) or the background (0).

Example PyTorch annotation for instance segmentation:

`'masks': torch.tensor([[[0, 0, 0], [0, 1, 1], [0, 0, 0]], [[0, 0, 0], [0, 0, 0], [1, 1, 0]]]), 'labels': torch.tensor([1, 2])`

## 3. Keypoint Annotation

Keypoint annotation involves identifying specific points of interest on an object, like joints in human pose estimation. Each keypoint is represented by its `x`, `y` coordinates, and a visibility flag.

### Format in PyTorch

In PyTorch, keypoints are represented as `[x, y, visibility]`, where:
- `x`, `y`: Coordinates of the keypoint.
- `visibility`: A flag indicating whether the keypoint is visible (1) or not visible (0).

Example PyTorch annotation for keypoint annotation:

`'keypoints': torch.tensor([[[150, 200, 1], [170, 220, 1], [190, 250, 0]]]), 'labels': torch.tensor([1])`

This format is commonly used in pose estimation tasks, where keypoints represent joints on a body.

## PyTorch Annotation Workflow

In a typical PyTorch workflow, annotations are stored in a dataset, where each image has a corresponding annotation that contains bounding boxes, masks, or keypoints. The dataset can then be used to train a model, such as Faster R-CNN (for object detection), Mask R-CNN (for segmentation), or HRNet (for pose estimation).

Here's a sample structure for an annotated image in PyTorch:

`'image': image, 'annotations': {'boxes': torch.tensor([[10, 20, 200, 400]]), 'labels': torch.tensor([1]), 'masks': torch.tensor([[[0, 0, 0], [0, 1, 1], [0, 0, 0]]]), 'keypoints': torch.tensor([[[150, 200, 1]]])}`

By leveraging these annotations, we can effectively train models for object detection, segmentation, and pose estimation in PyTorch.

---

## Conclusion

Annotated data is the foundation of any successful computer vision model. Without precise labeling, the algorithm would struggle to identify and differentiate objects within an image. Whether you're working with bounding boxes, instance segmentation, or keypoint annotations, each method serves a specific purpose in guiding the model to understand and predict object locations and relationships. 