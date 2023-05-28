Certainly! Here's the updated document with the complete installation instructions:

## 1. Installation

### 1.1 Environment
The environment is tested with Ubuntu 20.04 and Python 3.8, with NVIDIA GPU plus CUDA enabled. For Windows users, follow the instructions below to set up the environment. We recommend using Anaconda or Miniconda to install the running environment.

1. Download Anaconda or Miniconda installer for Windows from the following links:
   - Anaconda: [https://docs.anaconda.com/anaconda/install/](https://docs.anaconda.com/anaconda/install/)
   - Miniconda: [https://conda.io/miniconda.html](https://conda.io/miniconda.html)

2. Once downloaded, run the installer and follow the instructions to complete the installation.

3. Download Visual Studio 2019 Community edition or the desired edition from the following link: [Visual Studio 2019 Downloads](https://my.visualstudio.com/Downloads?q=visual%20studio%202019&wt.mc_id=o~msft~vscom~older-downloads)

4. Sign in with your Microsoft account or create a new one if you don't have an account.

5. Scroll through the list of available downloads and select the edition of Visual Studio 2019 that suits your needs (e.g., Visual Studio 2019 Community, Visual Studio 2019 Professional, or Visual Studio 2019 Enterprise).

6. Click on the "Download" button next to the selected edition to start the download.

7. Once the download is complete, run the downloaded installer.

8. During the installation process, you will be presented with various components and workloads to choose from. Make sure to select "Desktop development with C++" workload.

9. Expand the "Desktop development with C++" workload and ensure the following options are selected:
   - "MSVC v142 - VS 2019 C++ x64/x86 build tools"
   - "Windows 10 SDK (10.0.x.x)"
   - "C++ MFC for latest v142 build tools (x86 & x64)"
   - "C++/CLI support"
   - "C++ modules for latest v142 build tools"

10. Additionally, search for "Clang Compiler for Windows" and make sure it is selected.

11. Proceed with the installation by following the on-screen instructions.

12. Download Git for Windows from the following link: [Git for Windows](https://git-scm.com/download/win)

13. Once the download is complete, run the Git installer and follow the instructions to complete the installation. Git provides a command-line interface and a graphical user interface (Git GUI) that makes it easier to work with Git repositories on Windows.

14. Download wget for Windows from the following link: [wget-1.21.4-win64.zip](https://eternallybored.org/misc/wget/releases/wget-1.21.4-win64.zip)

15. Once the download is complete, extract the contents of the ZIP file to a folder of your choice. For example, you can create a folder called `wget` in your desired location and extract the contents there.

16. Open the Start menu, search for "Environment Variables," and select the "Edit the system environment variables" option.

17. In the System Properties window, click on the "Environment Variables" button.

18. In the Environment Variables window, under the "System variables" section, scroll down and find the "Path" variable. Select it and click the "Edit" button.

19. In the Edit Environment Variable window, click the "New" button to add a new entry.

20. Enter the path to the folder where

 you extracted the wget executable (e.g., `C:\path\to\wget.exe`) and click "OK."

21. Click "OK" to close all the open windows.

22. After installing MSVC 19, Git, and wget, open Anaconda Prompt or the command prompt and create a new conda environment by executing the following command:
    ```
    conda create -n e4s python=3.8
    ```

23. Activate the newly created environment:
    ```
    conda activate e4s
    ```

24. Clone or download the project code to your local machine.

25. Navigate to the project directory using the command prompt:
    ```
    cd path/to/project/directory
    ```

26. Install the required dependencies by executing the following command:
    ```
    conda env create -f e4s_env_win.yaml
    ```

### 1.2 Pre-trained model
For Windows users, follow the steps below to download and place the pre-trained RGI model in the appropriate folder.

1. Download the pre-trained RGI model from this [Google Drive link](https://drive.google.com/file/d/1cyJTYRO5G4kcugAcgSJ7cMsE96GzV_hq/view?usp=share_link).

2. Locate the downloaded model file and place it in the `pretrained_ckpts/e4s` folder within the project directory.

### 1.3 Other dependencies

#### 1.3.1 Face Parser

To use the face parser for facial segmentation, follow the steps below:

1. Download the face-parsing.PyTorch pre-trained model from [this link](https://drive.google.com/open?id=154JgKpzCPW82qINcVieuPH3fZ2e0P812).

2. Place the downloaded model file in the `pretrained_ckpts/face_parsing` folder within the project directory.

Alternatively, if you want to use the SegNeXt-FaceParser, follow the steps below:

1. Download the pre-trained SegNeXt model:
   - Small: [https://drive.google.com/file/d/1FJDN1edNpUyx8Bv5Eo7JutAvbL9zFfn4/view?usp=share_link](https://drive.google.com/file/d/1FJDN1edNpUyx8Bv5Eo7JutAvbL9zFfn4/view?usp=share_link)
   - Base: [https://drive.google.com/file/d/1YL4VuCBhhl-sjI3oPZOJhxTf9rIJRxD5/view?usp=share_link](https://drive.google.com/file/d/1YL4VuCBhhl-sjI3oPZOJhxTf9rIJRxD5/view?usp=share_link)

2. Place the downloaded SegNeXt model files in the `pretrained_ckpts/face_parsing` folder within the project directory.

#### 1.3.2 FaceVid2Vid

To use the FaceVid2Vid face reenactment model, follow the steps below:

1. Download the pre-trained model (Vox-256-New) from [this link](https://www.mediafire.com/folder/fcvtkn21j57bb/TalkingHead_Update).

2. Place the downloaded model file in the `pretrained_ckpts/facevid2vid` folder within the project directory.

#### 1.3.3 GPEN

To use the GPEN face restoration model, follow the steps below:

1. Download the following pre-trained models:
   - RetinaFace-R50 for face detection: [https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/RetinaFace-R50.pth](https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/RetinaFace-R50.pth)
   - RealESRNet_x4 for x4 super resolution: [https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/realesrnet_x4.pth](https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/realesrnet_x4.pth)
   - GPEN-BFR-512 (GPEN pre-trained model): [https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/GPEN-BFR-512.pth](https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/GPEN-BFR-512.pth)
   - ParseNet for face parsing: [https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/ParseNet-latest.pth](https://public-vigen-video.oss-cn-shanghai.aliyuncs.com/robin/models/ParseNet-latest.pth)

2. Place these downloaded checkpoint files into the `pretrained_ckpts/gpen` folder within the project directory.

Alternatively, you can execute the following script to automatically fetch these models:
```sh
cd pretrained_ckpts/gpen
sh ./fetch_gpen_models.sh
```

### 1.4 Git
To work with Git repositories and version control, it is recommended to install Git for Windows. You can download Git for Windows from the following link:

[Git for Windows](https://git-scm.com/download/win)

Click on the link to download the Git installer, and once the download is complete, run the installer and follow the instructions to install Git on your Windows system.

### 1.5 Wget
To install wget for Windows and add its path to the Windows system environment variables, follow the steps below:

1. Download wget for Windows from the following link: [wget-1.21.4-win64.zip](https://eternallybored.org/misc/wget/releases/wget-1.21.4-win64.zip)

2. Once the download is complete, extract the contents of the ZIP file to a folder of your choice. For example, you can create a folder called `wget` in your desired location and extract the contents there.

3. Open the Start menu, search for "Environment Variables," and select the "Edit the system environment variables" option.

4. In the System Properties window, click on the "Environment Variables" button.

5. In the Environment Variables window, under the "System variables" section, scroll down and find the "Path" variable. Select it and click the "Edit" button.

6. In the Edit Environment Variable window, click the "New" button to add a new entry.

7. Enter the path to the folder where you extracted the wget executable (e.g., `C:\path\to\wget`) and click "OK."

8. Click "OK" to close all the open windows.

9. Open a new command prompt window, or restart your existing command prompt, and you should now be able to use the `wget` command.

Note: Make sure to replace `C:\path\to\wget.exe` with the actual path to the folder where you extracted the wget executable.

After following these steps, you should have the necessary environment, MSVC 19, Git, and wget installed on your Windows system and be ready

 to use the software.

## 2. Sanity check
After completing the installation and placing the required checkpoint files, verify that your `pretrained_ckpts` folder structure matches the following:

```sh
pretrained_ckpts/
├── auxiliray
│   ├── model_ir_se50.pth
│   └── model.pth
├── e4s
│   └── iteration_300000.pt
├── face_parsing
│   ├── 79999_iter.pth
│   ├── segnext.base.512x512.celebamaskhq.160k.py
│   ├── segnext.base.best_mIoU_iter_140000.pth (optional)
│   ├── segnext.small.512x512.celebamaskhq.160k.py
│   └── segnext.small.best_mIoU_iter_140000.pth (optional)
├── facevid2vid (optional)
│   ├── 00000189-checkpoint.pth.tar
│   └── vox-256.yaml
├── gpen (optional)
│   ├── fetch_gepn_models.sh
│   └── weights
│       ├── GPEN-BFR-512.pth
│       ├── ParseNet-latest.pth
│       ├── realesrnet_x4.pth
│       └── RetinaFace-R50.pth
├── put_ckpts_accordingly.txt
└── stylegan2
    └── stylegan2-ffhq-config-f.pt
```

Make sure to verify the presence of all the necessary files and folders in the `pretrained_ckpts` directory.
