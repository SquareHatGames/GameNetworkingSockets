delete folders
- build
- vcpkg
- vcpkg_installed

git clone https://github.com/microsoft/vcpkg
.\vcpkg\bootstrap-vcpkg.bat
.\vcpkg\vcpkg install --triplet=x64-windows-static
cmake -S . -B build -DBUILD_EXAMPLES=OFF -DBUILD_TESTS=OFF -DUSE_STEAMWEBRTC=ON -DOPENSSL_USE_STATIC_LIBS=ON -DProtobuf_USE_STATIC_LIBS=ON -DVCPKG_TARGET_TRIPLET=x64-windows-static -DBUILD_STATIC_LIB=ON -DBUILD_SHARED_LIB=OFF
