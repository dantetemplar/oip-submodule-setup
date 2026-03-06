### Run on Linux

#### From prepared files in [Releases](https://github.com/promoblako/oip-setup/releases):

TODO

#### From Sources:

  1. Clone patched godot repository:
      
    ```bash
    git clone --depth 1 https://github.com/Open-Industry-Project/godot.git
    ```

  2. Build godot from [docs](https://docs.godotengine.org/en/latest/engine_details/development/compiling/compiling_for_linuxbsd.htmlg/)

  3. Download default_project.zip from [releases](https://github.com/Open-Industry-Project/Open-Industry-Project/releases)

    ```bash
    curl -L https://github.com/Open-Industry-Project/Open-Industry-Project/releases/download/v4.6-stable/OIP_v4.6-stable.zip -o OIP_v4.6-stable.zip
    ```

    ```bash
    unzip OIP_v4.6-stable.zip
    ```

    ```bash
    mv OIP_v4.6-stable/default_project.zip default_project.zip
    ```
