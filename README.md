# RN 0.61 with Fresco patch to disable image downsampling

## Setup

1. Clone this repository within your `<ProjectName>` directory:
```
git clone https://github.com/clytras/RN061FrescoBuild.git <ProjectName>
cd <ProjectName>
```

2. Install modules and run `fresco-setup` script:

```
yarn install
yarn fresco-setup
```

3. Download and unzip/install [Android NDK Revision 19c](https://developer.android.com/ndk/downloads/older_releases.html). I have downloaded [`android-ndk-r19c-windows-x86_64.zip`](https://dl.google.com/android/repository/android-ndk-r19c-windows-x86_64.zip) and unzipped it under `G:\Dev\Android\android-ndk-r19c` on Windows.

4. Create `android/libraries/fresco/local.properties` with the following contents:

```
ndk.dir=G:\\Dev\\Android\\android-ndk-r19c
org.gradle.daemon=true
org.gradle.parallel=true
org.gradle.configureondemand=true
```

Remember to change `ndk.dir` to the actual path that you've installed NDK R19C.

5. Open an Android Emulator and build the app:

```
yarn android
```

## Screenshots

| Before patch/build | After patch/build |
|------------------------------------|-------|
|![Before Fresco patch](https://raw.githubusercontent.com/clytras/RN061FrescoBuild/master/assets/RN061FrescoBuild_before_patch.png)|![After Fresco patch](https://raw.githubusercontent.com/clytras/RN061FrescoBuild/master/assets/RN061FrescoBuild_after_patch.png)|
