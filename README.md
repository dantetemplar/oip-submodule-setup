> [!CAUTION]
> NOT WORKING YET!!!

### Run

In order to run you should have godot executable and `default_project.zip` in the root directory (see [Build `godot` on Linux](#build-godot-on-linux) section). For Windows setup just go to [Open-Industry-Project/Open-Industry-Project](https://github.com/Open-Industry-Project/Open-Industry-Project) and download `default_project.zip` from releases.

Run binary (`./godot.linuxbsd.editor.x86_64`), click new project and use defaults.

### Build `godot` on Linux

#### From prepared files in [Releases](https://github.com/promoblako/oip-setup/releases):

Just go and download `default_project.zip` and `godot.linuxbsd.editor.x86_64` from [Releases](https://github.com/promoblako/oip-setup/releases) and move them to the root directory.

#### Build from Sources:

  1. Clone patched `godot` repository:
      
    ```bash
    git clone --depth 1 https://github.com/Open-Industry-Project/godot.git
    ```


  2. Build `godot` from [docs](https://docs.godotengine.org/en/latest/engine_details/development/compiling/compiling_for_linuxbsd.html)


  3. Move executable to root directory:

    ```bash
    mv godot/bin/godot.linuxbsd.editor.x86_64 godot.linuxbsd.editor.x86_64
    ```

    ```bash
    chmod +x godot.linuxbsd.editor.x86_64
    ```

  4. Clone patched Open-Industry-Project repository with support for linux and make `default_project.zip` from it:
  
    Clone repository:
    ```bash
    git clone --depth 1 https://github.com/Lucas-Alf/Open-Industry-Project.git
    ```

    Enter repository and rebase so it will be up to date with the [main repo](https://github.com/Open-Industry-Project/Open-Industry-Project)
    
    ```bash
    cd Open-Industry-Project
    git remote add upstream https://github.com/Open-Industry-Project/Open-Industry-Project.git
    git fetch upstream
    git rebase upstream/main
    ```

    Make `default_project.zip` from it:
    
    ```bash
    cd ..
    rsync -a --exclude='.git' Open-Industry-Project/ default_project/ && zip -r default_project.zip default_project && rm -rf default_project
    ```

<!-- 
  3. Download `default_project.zip` from [releases](https://github.com/Open-Industry-Project/Open-Industry-Project/releases)

    ```bash
    curl -L https://github.com/Open-Industry-Project/Open-Industry-Project/releases/download/v4.6-stable/OIP_v4.6-stable.zip -o OIP_v4.6-stable.zip
    ```

    ```bash
    unzip OIP_v4.6-stable.zip
    ```

    ```bash
    mv OIP_v4.6-stable/default_project.zip default_project.zip
    ```

    ```bash
    rm OIP_v4.6-stable.zip
    ```

    ```bash
    rm -rf OIP_v4.6-stable
    ``` -->
