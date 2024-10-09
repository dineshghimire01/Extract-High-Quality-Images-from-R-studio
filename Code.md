# Line 1: Set up a TIFF/SVG device to save the plot with specified dimensions and resolution
tiff('/path/to/your/directory/effect.tiff', 'effect.tiff', units = "in", width = 12, height = 8, res = 300)

                         #OR
                         
svg('/path/to/your/directory/effect.svg', width = 10, height = 10)

 This creates a rectangular image of size 12x8 inches at 300 DPI, suitable for high-quality posters or manuscript figures.

 You can adjust the width, height, and resolution to fit your specific needs for different publications.

# Line 2: Generate the plot using ggplot (or other plotting functions)
ggplot(data, aes(x, y)) + geom_point() + theme_minimal() # Customize your plot as required (e.g., colors, themes, labels)

# Line 3: Close the TIFF device and save the image to the local machine (computer, laptop)
dev.off()
