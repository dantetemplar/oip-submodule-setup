Clone that repository, lfs, and symlinks:
```
git clone https://github.com/dantetemplar/oip-submodule-setup.git --recurse --shallow-submodules
cd oip-setup
git submodule update --init --recursive
git lfs pull
```

Download prepared godot binary for [Windows here](https://github.com/Open-Industry-Project/Open-Industry-Project/releases/download) or build manually for Linux(maybe in future Open-Industry-Project will have binary for linux and windows in its repo).

Run binary `./godot.linuxbsd.editor.x86_64 --editor --path .` to open editor in current directory.

Note that you should not edit Open-Industry-Project project folder unless you want to contribute to the project. Make all changes in some your folder, you could inherence nodes from Open-Industry-Project folder (they all are mapped to `assets`, `parts`, `src` res folders via symlinkins). Also in future we should replace ours git submodule to upstream Open-Industry-Project repository.
