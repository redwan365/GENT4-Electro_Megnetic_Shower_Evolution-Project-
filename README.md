# Geant4 Electro-Magnetic Shower Evolution Project

This repository presents a complete Geant4-based simulation framework
to study the **Electro-Magnetic Shower Evolution** in matter.

The project includes:
- Full Geant4 v11.4.0 installation on macOS (Apple Silicon)
- Example-based simulation (B1)
- EM shower hit distributions
- Energy deposition estimation methodology
- Research-ready documentation

---

## System Configuration
- OS: macOS (Apple Silicon – M1/M2/M3/M4)
- Geant4: v11.4.0 (source build)
- Compiler: AppleClang
- Build system: CMake
- Visualization: Qt + OpenGL

---

## Installation Summary

```bash
brew install cmake qt
xcode-select --install

mkdir -p ~/geant4/build ~/geant4/install
cd ~/geant4/build

cmake ~/Downloads/geant4-v11.4.0 \
  -DCMAKE_INSTALL_PREFIX=~/geant4/install \
  -DGEANT4_INSTALL_DATA=ON \
  -DGEANT4_USE_QT=ON

make -j$(sysctl -n hw.ncpu)
make install
source ~/geant4/install/bin/geant4.sh

brew install qt
