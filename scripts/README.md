# Install necessary packages (run once if not already installed)

install.packages("gplots")
install.packages("ggplot2")

**Load required library**

library(gplots)

 **Set working directory (adjust path as needed)**
 
setwd('Z:\\My Folders\\Desktop\\WORKSHOP\\research\\module 5\\')

# Read the data file (make sure strain names are in the first column)
data <- read.csv("Strain Vs Antibiotics.csv", header = TRUE, row.names = 1, stringsAsFactors = FALSE)

# Check if row names are correctly set to strain names
head(rownames(data))  # Should show strain names

# Transpose the data and ensure strain names are correctly used as row names
data_transposed <- t(data)
rownames(data_transposed) <- colnames(data)   # Strains as row names
colnames(data_transposed) <- rownames(data)   # Antibiotics as column names

# Check row names and column names
head(rownames(data_transposed))  # Strains
head(colnames(data_transposed))  # Antibiotics

# Define custom color palette (black -> green -> red)
my_palette <- colorRampPalette(c("black", "green", "red"))(256)

# Save the heatmap as an image
png("Strain_Vs_Antibiotics_Debug.png", width = 1600, height = 1000)

# Create heatmap
heatmap.2(data_transposed,
  col = my_palette,        # Custom color palette
  Colv = FALSE,            # Don't reorder columns
  Rowv = FALSE,            # Don't reorder rows
  dendrogram = "none",     # No dendrograms
  trace = "none",          # Disable trace lines
  margins = c(5, 10),      # Adjust margins
  cexRow = 0.8,            # Row label size
  cexCol = 0.8,            # Column label size
  key = TRUE,              # Display color key
  keysize = 0.5,           # Adjust key size
  key.title = NULL,        # No key title
  key.xlab = NULL,         # No x-axis label for key
  key.ylab = NULL,         # No y-axis label for key
  density.info = "none",   # Disable density info
  las = 2                  # Rotate x-axis labels
)

# Close graphics device (saves the file)
dev.off()

