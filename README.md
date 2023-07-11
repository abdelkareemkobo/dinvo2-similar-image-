# dinvo2-similar-image

This project allows you to search for similar images in your dataset or find similar artwork like on the Pinterest website using Dinov2 with Faiss.

![:)](dino_demo.gif)

## Usage

1. Install the required dependencies:
   - `faiss-gpu`
   - `torch`
   - `torchvision`
   - `PIL`
   - `numpy`
   - `matplotlib`
   - `gradio`

2. Load the DINO model:
   - Use the Dinov2 implementation from Facebook Research.

3. Define the image transformations for preprocessing:
   - Resize the images to (224, 224) pixels.
   - Convert the images to tensors.
   - Normalize the image tensors.

4. Implement the `extract_features` function:
   - Extract features from an input image using the DINO model.

5. Use the `nearest_neighbor_search` function:
   - Perform nearest neighbor search using Faiss.
   - Retrieve the indices of the nearest neighbor images.

6. Implement the `return_nearest_neighbor_images` function:
   - Return the paths of the nearest neighbor images based on the query image.

7. Create a Gradio interface:
   - Use `gradio` to create an interface for uploading an image and displaying the nearest neighbor images.

## TODO

- [ ] Add illustrations for the concept (dinov2, instance retrieval, faiss)
- [ ] Explore possible optimizations for search and encoding
- [ ] Implement a pipeline to generate captions based on the input image and its nearest neighbor using NLP
- [ ] Upload the project to HuggingFace space as a demo
- [ ] Save Faiss state for future use

Remember to set the `dataset_path` variable to the path of your dataset before running the Gradio interface.

Enjoy finding similar images and artwork with Dinov2 and Faiss!