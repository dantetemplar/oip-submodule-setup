Clone that repository https://github.com/promoblako/oip-setup with submodules, lfs, and symlinks:
```
git clone https://github.com/promoblako/oip-setup.git --recurse --shallow-submodules
cd oip-setup
git submodule update --init --recursive
git lfs pull
```

Download prepared godot binary for [Windows here](https://github.com/Open-Industry-Project/Open-Industry-Project/releases/download) for [linux here](https://github.com/promoblako/oip-setup/releases) (maybe in future Open-Industry-Project will have binary for linux and windows in its repo).

Run binary `./godot.linuxbsd.editor.x86_64 --editor --path .` to open editor in current directory.

Note that you should not edit Open-Industry-Project project folder unless you want to contribute to the project. Make all changes in `promoblako` folder, you could inherence nodes from Open-Industry-Project folder (they all are mapped to `assets`, `parts`, `src` res folders via symlinkins). Also in future we should replace ours git submodule to upstream Open-Industry-Project repository.
