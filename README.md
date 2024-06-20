# Movie Storybook with PIL (Pillow)

This Jupyter Notebook project creates a movie storybook using the `PIL` (Pillow) package in Python. The storybook is composed of images with text annotations, describing scenes from a movie. This project demonstrates how to use `PIL` for image manipulation, including loading images, adding text, and saving the final output.

## Notebook Features

- **Loading Images**: Import and display images that will be used in the storybook.
- **Adding Text**: Annotate images with descriptive text using various fonts and styles.
- **Image Manipulation**: Use `PIL` functionalities to manipulate images, such as resizing, cropping, and adjusting colors.
- **Saving Images**: Save the edited images to create a cohesive storybook.

## Example Workflow

1. **Importing Libraries**: Import necessary libraries, primarily `PIL`, for image processing.
2. **Loading an Image**: Load an image from a file and display it.
3. **Annotating the Image**: Add text to the image using `ImageDraw` and `ImageFont` modules from `PIL`.
4. **Displaying the Image**: Display the edited image with annotations.
5. **Saving the Image**: Save the final image to a file.

## Example Code

Here is a snippet of code demonstrating how to add text to an image using `PIL`:

```python
from PIL import Image, ImageDraw, ImageFont

# Load an image
image = Image.open('path/to/your/image.jpg')

# Initialize ImageDraw
draw = ImageDraw.Draw(image)

# Define text and font
text = "This is a scene from the movie."
font = ImageFont.truetype('arial.ttf', size=45)

# Define text position
text_position = (50, 50)

# Add text to image
draw.text(text_position, text, font=font, fill="white")

# Show the image
image.show()

# Save the edited image
image.save('path/to/save/edited_image.jpg')
