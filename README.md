# ImageNet-objects
# Jetson Nano Custom Object Classification with ImageNet

This project demonstrates how to use the **Jetson Nano** and **Jetson Inference's ImageNet model** to classify **custom  tools and objects cars** using your own dataset. Instead of relying on default classes, we trained and tested against personalized images placed in the Jetson Inference `data/images/` directory.

---

 Project Overview

- Goal: Recognize and label random household tools or objects using a pretrained ImageNet classifier on the Jetson Nano.
- **Approach**: Run `imagenet` inference commands on custom images and output annotated results.
- **Creativity**: Uses a **custom dataset**, not default ImageNet images. This demonstrates how ImageNet can generalize to unique real-world inputs.

---

##  Location

 dataset is stored in the following directory on the Jetson Nano:

/home/nvidia11/jetson-inference/data/images/

markdown
Copy
Edit

- Input images (e.g. `object_0.jpg`, `object_1.jpg`) are used for classification.
- Output images (e.g. `final1.jpg`, `final2.jpg`) are labeled with predictions.

Example file structure:
data/images/
├── object_0.jpg
├── object_1.jpg
├── ...
├── final1.jpg
├── final2.jpg

 How to Run


```bash
# Run inference on an image
imagenet /home/nvidia11/jetson-inference/data/images/object_0.jpg /home/nvidia11/jetson-inference/data/images/final1.jpg

