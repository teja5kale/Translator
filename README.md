#  STL to .dat Translator

## Project Description

This project reads a cube STL file, processes its vertex data, and writes the corresponding points into a `.dat` file for visualization purposes. The program utilizes C++ classes to handle the reading of STL files, the conversion of vertex points, and the triangulation of data for graphical representation using tools like Gnuplot.

## Project Structure

The project is organized into multiple classes to separate concerns for better scalability and maintainability. Below is the structure of the project:


## Classes Overview

1. **Point Class**:
   - Represents a point in 3D space.
   - Stores coordinates as `x`, `y`, and `z`.
   - Contains methods to retrieve point coordinates.

2. **Reader Class**:
   - Reads an STL file (`cube-ascii.stl`).
   - Processes vertex data, stores unique points, and maps them to indices using an unordered map.
   - Returns a list of unique `Point` objects.

3. **Triangle Class**:
   - Represents a triangle composed of three `Point` objects.
   - Contains methods to retrieve triangle vertices' coordinates.

4. **Triangulation Class**:
   - Groups points into sets of three, forming triangles.
   - Returns a vector of `Triangle` objects.

5. **Writer Class**:
   - Writes the triangle vertex data into a `.dat` file.
   - Ensures that the output format is suitable for Gnuplot or other visualization tools.

## How to Compile and Run

1. **Compilation**:
   - Compile the source code using any standard C++ compiler (e.g., `g++`).
   ```bash
   g++ main.cpp Point.cpp Reader.cpp Triangle.cpp Triangulation.cpp Writer.cpp -o CubeToDat
