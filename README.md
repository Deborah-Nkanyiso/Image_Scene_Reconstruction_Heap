# Image Scene Reconstruction using Heap

A Java application that reconstructs a complete scene image by extracting 8x8 patches from multiple input images, using perceptual hashing and a **min-heap** to select the best patches.

**Author:** DN MBOYI  
**Student Number:** 222019179  
**Assignment:** Heap & Image Processing  
**Course:** CSC03B3 (Data Structures / Java Programming)

---

## Project Description

This program performs **image mosaicing / scene reconstruction** by:
- Extracting 8x8 grayscale patches from multiple input images
- Computing perceptual hash (average hash - aHash) for each patch
- Using a custom **Heap** (min-heap) to efficiently select the top patches based on hash similarity
- Reconstructing a final 800x800 image by placing the best patches in their original positions

---

## Features

- **Custom Heap** implementation (extends `BinaryTree`)
  - `insert()` with upheap
  - `removeMin()` with downheap
- **PositionList** for managing patches
- **Patch** extraction (8x8 grayscale blocks)
- **Perceptual Hashing** (aHash) for patch comparison
- **Image Reconstruction** (`renderScene`)
- Binary tree-based heap with proper last node tracking
- Efficient heap operations for large numbers of patches

---

## Files Included

- `Main.java` – Main program with patch extraction, heap usage, and image reconstruction
- `Heap.java` – Custom min-heap implementation (extends `BinaryTree`)
- Supporting classes (from JAR):
  - `BinaryTree.java`, `BTNode.java`, `Entry.java`
  - `PositionList.java`, `Position.java`, `Patch.java`

---

## Technologies Used

- **Heap Data Structure** (Binary Heap via Complete Binary Tree)
- **Upheap & Downheap** operations
- **Image Processing** with `BufferedImage`
- **Perceptual Hashing** (aHash)
- **Position-based ADT** (`Position`, `PositionList`)
- **Object-Oriented Design**

---

## How to Run

### Requirements:
- Place your input images in a folder named `scenes/` (`.jpg` files)
- Ensure all supporting classes from `p07 (1).jar` are in the classpath

### Compile and Run:
```bash
javac *.java
java Main
