# Implementing-a-RayTracer-in-C++-
RayTracing In One Weekend


# 2. Output an Image
## 2.1 The PPM Image Format
To see an image, easy way is to write it to a file. There are many formats, one of the format that is a plain text format is a ppm file.
The PPM format, there is a newline character at the end of the line and we use RGB to tell the color values.
![image](https://user-images.githubusercontent.com/48233453/147514065-4ded59b2-ab3c-40ec-ab19-058df4ad7e4a.png)

![image](https://user-images.githubusercontent.com/48233453/147517969-0da9d704-fd50-4dd0-9d62-b628c01dc263.png)
1. The pixels are written out in rows with pixels left to right.
2. The rows are written from the top to the bottom.
3. The RGB values range from 0 to 1. Since we are not working with high dynamic range, we will tonemap the output to the 0 to 1 range.


##  2.2 Creating an Image file
The code above will output the program output to stdout. But we want to redirect the output to a file. this can be done using this command on Windows.
```
C:\Users\arfasaif\Documents\Raytracing-In-Weekend\out\build\x64-Debug\Raytracing-In-Weekend.exe > image.ppm
```
You can open the file using an app called `Irfanview` or `ToyViewer` on Mac.
![image](https://user-images.githubusercontent.com/48233453/147517673-0317ae0f-ade1-4a78-9db4-c8b51e3465e4.png)

When we open the file in a text editor, it looks like this.
![image](https://user-images.githubusercontent.com/48233453/147517888-e49b51a2-c8f0-4da4-b3c8-863c6107c9ca.png)

