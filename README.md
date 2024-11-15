# text.mp4

**text.mp4** is a project that takes a video as input, converts each frame into ASCII art using any font you want, and generates a text-based video output along with the ASCII frames.

**Example** (takes a few seconds to load):
![Video Example](public/sampletxt.gif)

## Requirements

- GNU `make`
- OpenCV4 (`libopencv-dev` in Ubuntu, `opencv` in Fedora and Arch)
- g++ compiler (for C++ engine)
- Python 3.x (for Python engine and video linking)
- pip3 (for installing Python dependencies)
- vtk, glew, fmt (if not installed already)

## Setup (UNIX systems)

1. Clone the repository:

```bash
  git clone https://github.com/yantavares/text.mp4.git
  cd text.mp4
```

2. If necessary, make `play.sh` executable:

```bash
  chmod +x play.sh
```

3. **(Optional)** Add your desired video file to the `videos` directory, or use the provided `SampleVideo.mp4`.

4. **(Optional)** Add your desired font (.ttf files) to the `fonts` directory, or use the provided `ComicMono.ttf`.

For non-UNIX systems, you need to install the dependencies manually. They are listed [here](#requirements).

You can also modify the `Makefile` to change the default C++ compiler or Python version.

## **Running the Project**

To run the project, use the `make` command:

```bash
   make
```

To run the generated text-based video in the terminal, use the `make play` command:

```bash
   make play
```

Observation: The `make play` command will only work on UNIX systems and will automatically resize the video to fit terminal size.

### Steps after running `make`:

1. **Select Font**:
   - Default is `Comic Mono`.
2. **Choose Font Size**:
   - Choose a font size between 2 and 20.
   - Default is 10.
3. **Provide Video Filename**:
   - You will be prompted to choose a video file from the `videos` directory.
   - Default is `SampleVideo.mp4`.
4. **Select whether to play the video in the terminal automatically**:
   - Default is `yes`.

_Observation_: If no input is provided, the default values will be used.

### Outputs

- The output will be available inside the `output` directory, which contains:
  - `frames/`: Each frame as an ASCII image.
  - `text/`: ASCII text representation of each frame as a text file.
  - `text.mp4`: The final text-based video output.

## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Please open an issue or a pull request for any changes or improvements.
