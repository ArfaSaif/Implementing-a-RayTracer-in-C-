# Implementing-a-RayTracer-in-C++-
RayTracing In One Weekend


# 2. Output an Image
## 2.1 The PPM Image Format
To see an image, easy way is to write it to a file. There are many formats, one of the format that is a plain text format is a ppm file.
The PPM format, there is a newline character at the end of the line and we use RGB to tell the color values.
![image](https://user-images.githubusercontent.com/48233453/147514065-4ded59b2-ab3c-40ec-ab19-058df4ad7e4a.png)

'''
#include <iostream>

int main() {

    // Image

    const int image_width = 256;
    const int image_height = 256;

    // Render

    std::cout << "P3\n" << image_width << ' ' << image_height << "\n255\n";

    for (int j = image_height-1; j >= 0; --j) {
        for (int i = 0; i < image_width; ++i) {
            auto r = double(i) / (image_width-1);
            auto g = double(j) / (image_height-1);
            auto b = 0.25;

            int ir = static_cast<int>(255.999 * r);
            int ig = static_cast<int>(255.999 * g);
            int ib = static_cast<int>(255.999 * b);

            std::cout << ir << ' ' << ig << ' ' << ib << '\n';
        }
    }
}

'''
