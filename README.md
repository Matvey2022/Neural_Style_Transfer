# Neural Style Transfer (NST)

Neural Style Transfer (NST) is a creative deep learning technique that combines two images into one. It takes the content of one image and merges it with the artistic style of another, producing a unique, visually stunning result.

This project implements NST using PyTorch, based on the foundational work of Gatys et al. For efficiency and quality, it uses a pre-trained VGG19 model to extract content and style features.

---

## What’s Inside

- Content + Style Extraction: We use a pre-trained VGG19 model to extract content and style features from the input images.
- Flexible Loss Functions: Combines content loss, style loss (using Gram matrices), and total variation loss for smooth and realistic results.
- Lightweight and Fast: Optimized with PyTorch and pre-trained weights for quick experimentation and high-quality outputs.

---

## How It Works

1. Input Images:
   - A content image provides the structure (what the image shows).
   - A style image provides the artistic flair (how the image looks).

2. Feature Extraction:
   - VGG19 is used to extract features:
     - Content Features: From deeper layers (capture structure and layout).
     - Style Features: From earlier layers (capture textures and patterns).

3. Optimization:
   - A randomly initialized image (the pastiche) is optimized using gradient descent to minimize:
     - Content Loss: Ensures the pastiche matches the content image.
     - Style Loss: Matches the pastiche’s texture to the style image.
     - Total Variation Loss: Reduces noise and creates smoother outputs.

---