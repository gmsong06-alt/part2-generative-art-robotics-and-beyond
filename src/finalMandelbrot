// Set the maximum number of iterations for the Mandelbrot calculation
int maxIterations = 255;

// Define the region of the Mandelbrot set to display
float xmin = -2;
float xmax = 2;
float ymin = -2;
float ymax = 2;

// Set up the canvas size
void setup() {
  size(800, 800);
  noLoop();
}

// Main drawing function
void draw() {
  // Prepare to update pixel data
  loadPixels();
  
  // Calculate the Mandelbrot set and update pixels
  calculateMandelbrot();
  
  // Display the updated pixels
  updatePixels();
  save("output.png");
}

// Function to calculate the Mandelbrot set
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

// Function to calculate the Mandelbrot value for a given point (c, z)
int calculateMandelbrotValue(float cx, float cy) {
  float zx = cx;
  float zy = cy;
  
  int n = 1;
  
  while (n < maxIterations) {
    if ((zx * zx + zy * zy) >= 4) {
      break;
    }
    
    n++;
    
    float origZx = zx;
    
    zx = zx * zx - zy * zy + cx;
    zy = (2 * origZx * zy) + cy;
    
  }
  
  return n;
}

color calculateColor(int n) {
  return color(n * 4, n/2, n * 6);
}

