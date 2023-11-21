// Set the maximum number of iterations for the Mandelbrot calculation
int maxIterations = 3;

// Define the region of the Mandelbrot set to display
float xmin = -2;
float xmax = 2;
float ymin = -2;
float ymax = 2;

// DO NOT CHANGE
void setup() {
  size(3, 3);
  noLoop();
}

// DO NOT CHANGE
void draw() {
  loadPixels();
  calculateMandelbrot();
  updatePixels();
}

// DO NOT CHANGE
void calculateMandelbrot() {
  // Loop through each pixel on the canvas
  for (int x = 0; x < width; x++) {
    for (int y = 0; y < height; y++) {
      
      float cx = x * (xmax - xmin) / (width - 1) + xmin;
      float cy = -(y * (ymax - ymin) / (height - 1) + ymin);
      
      float zx = cx;
      float zy = cy;
      
      // Calculate the Mandelbrot value for the current pixel
      int n = calculateMandelbrotValue(cx, cy);
       
      // Map the Mandelbrot value to a brightness value
      color pixelColor = calculateColor(n);
      
      // Calculate the pixel index
      int pix = x + y * width;
      
      // Set the pixel color based on the brightness
      pixels[pix] = pixelColor;
    }
  }
}

// FINISH THE FUNCTION
int calculateMandelbrotValue(float cx, float cy) {
  float zx = cx;
  float zy = cy;
  
  int n = 1;
  
  while (n < maxIterations) {
    // STEP 1: Implement Formula A
  }
  
  return n;
}

// FINISH THE FUNCTION
color calculateColor(int n) {
  // STEP 2: Implement the logic for coloring pixels (red, green, and blue)
}
