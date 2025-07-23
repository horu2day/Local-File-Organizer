네, 해당 소스 코드(프로젝트)에 대한 설명을 한국어로 번역하고 정리해 드리겠습니다.

---

## 로컬 파일 정리기: AI 파일 관리, 100% 당신의 기기에서, 개인정보 보호 보장

디지털 파일이 어지럽게 흩어져 있어 정리에 어려움을 겪고 계신가요? 이제 AI에게 힘든 일을 맡겨보세요! **로컬 파일 정리기**는 최첨단 AI 기술을 활용하여 여러분의 파일들을 깔끔하게 정리해 주는 개인 비서입니다. 가장 중요한 점은, 모든 과정이 여러분의 컴퓨터 안에서만 이루어져 개인정보를 완벽하게 보호한다는 것입니다.

### 작동 방식 엿보기

```
--------------------------------------------------
모델이 이미 다운로드되었는지 확인합니다. 없다면 지금 다운로드합니다.
**----------------------------------------------**
**       이미지 추론 모델 초기화 완료      **
**       텍스트 추론 모델 초기화 완료      **
**----------------------------------------------**
정리할 디렉터리 경로를 입력하세요: /home/user/documents/input_files
--------------------------------------------------
정리된 파일과 폴더를 저장할 경로를 입력하세요 (Enter를 누르면 입력 디렉터리 내에 'organized_folder'를 사용합니다)
출력 경로가 성공적으로 업로드되었습니다: /home/user/documents/organzied_folder
--------------------------------------------------
파일 경로를 불러오는 데 걸린 시간: 0.00초
--------------------------------------------------
이름 변경 전 디렉터리 구조:
/정리할/파일이/있는/경로
├── image.jpg
├── document.pdf
├── notes.txt
└── 하위_디렉터리
    └── picture.png

1개 디렉터리, 4개 파일
*****************
파일이 성공적으로 업로드되었습니다. 처리에는 몇 분 정도 소요될 수 있습니다.
*****************
파일: /정리할/파일이/있는/경로/image1.jpg
설명: [AI가 생성한 설명]
폴더명: [AI가 생성한 폴더명]
생성된 파일명: [AI가 생성한 파일명]
--------------------------------------------------
파일: /정리할/파일이/있는/경로/document.pdf
설명: [AI가 생성한 설명]
폴더명: [AI가 생성한 폴더명]
생성된 파일명: [AI가 생성한 파일명]
--------------------------------------------------
... [추가 파일 처리]
복사 및 이름 변경 후 디렉터리 구조:
/정리된/파일을/저장할/경로
├── 카테고리1
│   └── 생성된_파일명.jpg
├── 카테고리2
│   └── 생성된_파일명.pdf
└── 카테고리3
    └── 생성된_파일명.png

3개 디렉터리, 3개 파일
```

### 주요 기능

이 지능형 파일 정리기는 언어 모델(LM)과 비전-언어 모델(VLM) 같은 고급 AI 모델의 힘을 활용하여 파일 정리 프로세스를 자동화합니다.

- **콘텐츠 이해**:
  - **텍스트 분석**: [Gemma-2-2B](https://nexaai.com/google/gemma-2-2b-instruct/gguf-q4_0/file) 언어 모델을 사용하여 텍스트 기반 콘텐츠를 분석 및 요약하고, 관련성 높은 설명과 파일명을 생성합니다.
  - **시각 콘텐츠 분석**: [LLaVA-v1.6](https://nexaai.com/liuhaotian/llava-v1.6-vicuna-7b/gguf-q4_0/file) 비전-언어 모델을 사용하여 이미지와 같은 시각적 파일을 해석하고, 문맥에 맞는 카테고리와 설명을 제공합니다.
- **자동 파일 정리**: AI가 생성한 카테고리를 기반으로 파일을 자동으로 폴더에 분류합니다.
- **지능형 메타데이터 생성**: 고급 AI 모델을 사용하여 설명과 파일명을 만듭니다.
- **다양한 파일 형식 지원**: 이미지, 텍스트 파일, PDF를 처리할 수 있습니다.
- **병렬 처리**: 멀티프로세싱을 활용하여 파일 처리 속도를 높입니다.
- **사용자 정의 가능한 프롬프트**: AI 모델에 사용하는 프롬프트를 사용자가 직접 수정할 수 있습니다.

무엇보다 가장 큰 장점은 모든 AI 처리가 [Nexa SDK](https://github.com/NexaAI/nexa-sdk)를 통해 **100% 여러분의 컴퓨터에서 로컬로 실행된다는 점**입니다. 인터넷 연결이 필요 없으며, 어떤 데이터도 컴퓨터 밖으로 나가지 않고, 외부 AI API도 필요 없습니다. 여러분의 파일은 완벽하게 비공개로 안전하게 유지됩니다.

### 지원하는 파일 형식

- **이미지:** `.png`, `.jpg`, `.jpeg`, `.gif`, `.bmp`
- **텍스트 파일:** `.txt`, `.docx`
- **PDF:** `.pdf`

### 사전 요구사항

- **운영체제:** Windows, macOS, Linux 호환
- **파이썬 버전:** Python 3.12
- **Conda:** Anaconda 또는 Miniconda 설치 필요
- **Git:** 저장소를 복제하기 위해 필요 (ZIP 파일로 다운로드 가능)

### 설치 방법

#### 1. 저장소 복제(Clone)

Git을 사용하여 이 저장소를 로컬 컴퓨터에 복제합니다.

```zsh
git clone https://github.com/QiuYannnn/Local-File-Organizer.git
```

또는 저장소를 ZIP 파일로 다운로드하여 원하는 위치에 압축을 풉니다.

#### 2. 파이썬 환경 설정

`local_file_organizer`라는 이름의 새 Conda 환경을 Python 3.12로 생성합니다.

```zsh
conda create --name local_file_organizer python=3.12
```

생성한 환경을 활성화합니다.

```zsh
conda activate local_file_organizer
```

#### 3. Nexa SDK 설치 🛠️

##### CPU 버전 설치

CPU 버전의 Nexa SDK를 설치하려면 다음을 실행하세요.

```bash
pip install nexaai --prefer-binary --index-url https://nexaai.github.io/nexa-sdk/whl/cpu --extra-index-url https://pypi.org/simple --no-cache-dir
```

##### GPU 버전 설치 (macOS - Metal)

macOS의 Metal을 지원하는 GPU 버전의 경우 다음을 실행하세요.

```bash
CMAKE_ARGS="-DGGML_METAL=ON -DSD_METAL=ON" pip install nexaai --prefer-binary --index-url https://nexaai.github.io/nexa-sdk/whl/metal --extra-index-url https://pypi.org/simple --no-cache-dir
```

**CUDA** 및 **AMD GPU** 지원에 대한 자세한 Nexa SDK 설치 지침은 공식 README의 [설치 섹션](https://github.com/NexaAI/nexa-sdk?tab=readme-ov-file#installation)을 참조하세요.

#### 4. 의존성 패키지 설치

프로젝트 디렉터리 내에서 `requirements.txt`를 사용하여 필요한 패키지들을 설치합니다.

```zsh
pip install -r requirements.txt
```

**참고:** 만약 특정 패키지 설치에 문제가 발생하면, 개별적으로 설치해 보세요.

```zsh
pip install nexa Pillow pytesseract PyMuPDF python-docx
```

### 스크립트 실행 방법

환경이 활성화되고 의존성 패키지가 모두 설치되었다면, 다음 명령어로 스크립트를 실행합니다.

```zsh
python main.py
```

스크립트는 다음 순서로 작동합니다:

1. **입력 경로 입력**: 정리하고 싶은 파일이 있는 디렉터리의 전체 경로를 입력합니다.
2. **출력 경로 입력**: 정리된 파일을 저장할 경로를 입력합니다. 경로를 입력하지 않고 Enter를 누르면, 입력 디렉터리 안에 `organzied_folder`라는 폴더를 만들어 사용합니다.
3. 입력 디렉터리의 파일 구조를 보여줍니다.
4. 파일 처리가 시작됨을 알립니다.
5. 각 파일을 처리하며 메타데이터(설명, 폴더명, 파일명)를 생성합니다.
6. 생성된 메타데이터를 기반으로 파일을 출력 디렉터리에 복사하고 이름을 변경합니다.
7. 처리가 완료된 후 출력 디렉터리의 파일 구조를 보여줍니다.

### 참고 사항

- **SDK 모델:**
  - 이 스크립트는 `NexaVLMInference`와 `NexaTextInference` 모델을 사용합니다.
  - 이 모델들을 사용하려면 모델 파일을 다운로드하거나 경로를 올바르게 설정해야 할 수 있습니다.
- **의존성 패키지:**
  - **pytesseract:** 시스템에 Tesseract OCR이 설치되어 있어야 합니다.
    - **macOS:** `brew install tesseract`
    - **Ubuntu/Linux:** `sudo apt-get install tesseract-ocr`
    - **Windows:** [Tesseract OCR Windows Installer](https://github.com/UB-Mannheim/tesseract/wiki)에서 다운로드
  - **PyMuPDF (fitz):** PDF 파일을 읽는 데 사용됩니다.
- **처리 시간:**
  - 파일의 수와 크기에 따라 처리 시간이 오래 걸릴 수 있습니다.
  - 이 스크립트는 성능 향상을 위해 멀티프로세싱을 사용합니다.
- **프롬프트 사용자 정의:**
  - `data_processing.py` 파일의 프롬프트를 수정하여 메타데이터 생성 방식을 변경할 수 있습니다.

### 라이선스

이 프로젝트는 MIT 라이선스와 Apache 2.0 라이선스, 두 가지 라이선스가 적용됩니다. 사용자는 이 프로젝트에 대해 두 라이선스 중 원하는 것을 선택하여 사용할 수 있습니다.

아래 영문

# Local File Organizer: AI File Management Run Entirely on Your Device, Privacy Assured

Tired of digital clutter? Overwhelmed by disorganized files scattered across your computer? Let AI do the heavy lifting! The Local File Organizer is your personal organizing assistant, using cutting-edge AI to bring order to your file chaos - all while respecting your privacy.

## A Glimpse of How It Works

```
--------------------------------------------------
Checking if the model is already downloaded. If not, downloading it now.
**----------------------------------------------**
**       Image inference model initialized      **
**       Text inference model initialized       **
**----------------------------------------------**
Enter the path of the directory you want to organize: /home/user/documents/input_files
--------------------------------------------------
Enter the path to store organized files and folders (press Enter to use 'organized_folder' in the input directory)
Output path successfully upload: /home/user/documents/organzied_folder
--------------------------------------------------
Time taken to load file paths: 0.00 seconds
--------------------------------------------------
Directory tree before renaming:
Path/to/your/input/files/or/folder
├── image.jpg
├── document.pdf
├── notes.txt
└── sub_directory
    └── picture.png

1 directory, 4 files
*****************
The files have been uploaded successfully. Processing will take a few minutes.
*****************
File: Path/to/your/input/files/or/folder/image1.jpg
Description: [Generated description]
Folder name: [Generated folder name]
Generated filename: [Generated filename]
--------------------------------------------------
File: Path/to/your/input/files/or/folder/document.pdf
Description: [Generated description]
Folder name: [Generated folder name]
Generated filename: [Generated filename]
--------------------------------------------------
... [Additional files processed]
Directory tree after copying and renaming:
Path/to/your/output/files/or/folder
├── category1
│   └── generated_filename.jpg
├── category2
│   └── generated_filename.pdf
└── category3
    └── generated_filename.png

3 directories, 3 files
```

## What It Does

This intelligent file organizer harnesses the power of advanced AI models, including language models (LMs) and vision-language models (VLMs), to automate the process of organizing files by:

- Scanning a specified input directory for files.
- Content Understanding:

  - **Textual Analysis**: Uses the [Gemma-2-2B](https://nexaai.com/google/gemma-2-2b-instruct/gguf-q4_0/file) language model (LM) to analyze and summarize text-based content, generating relevant descriptions and filenames.
  - **Visual Content Analysis**: Uses the [LLaVA-v1.6](https://nexaai.com/liuhaotian/llava-v1.6-vicuna-7b/gguf-q4_0/file) vision-language model (VLM), based on Vicuna-7B, to interpret visual files such as images, providing context-aware categorization and descriptions.

- Understanding the content of your files (text, images, and more) to generate relevant descriptions, folder names, and filenames.
- Organizing the files into a new directory structure based on the generated metadata.

The best part? All AI processing happens 100% on your local device using the [Nexa SDK](https://github.com/NexaAI/nexa-sdk). No internet connection required, no data leaves your computer, and no AI API is needed - keeping your files completely private and secure.

We hope this tool can help bring some order to your digital life, making file management a little easier and more efficient.

## Features

- **Automated File Organization:** Automatically sorts files into folders based on AI-generated categories.
- **Intelligent Metadata Generation:** Creates descriptions and filenames using advanced AI models.
- **Support for Multiple File Types:** Handles images, text files, and PDFs.
- **Parallel Processing:** Utilizes multiprocessing to speed up file processing.
- **Customizable Prompts:** Prompts used for AI model interactions can be customized.

## Supported file types

- **Images:** `.png`, `.jpg`, `.jpeg`, `.gif`, `.bmp`
- **Text Files:** `.txt`, `.docx`
- **PDFs:** `.pdf`

## Prerequisites

- **Operating System:** Compatible with Windows, macOS, and Linux.
- **Python Version:** Python 3.12
- **Conda:** Anaconda or Miniconda installed.
- **Git:** For cloning the repository (or you can download the code as a ZIP file).

## Installation

### 1. Clone the Repository

Clone this repository to your local machine using Git:

```zsh
git clone https://github.com/QiuYannnn/Local-File-Organizer.git
```

Or download the repository as a ZIP file and extract it to your desired location.

### 2. Set Up the Python Environment

Create a new Conda environment named `local_file_organizer` with Python 3.12:

```zsh
conda create --name local_file_organizer python=3.12
```

Activate the environment:

```zsh
conda activate local_file_organizer
```

### 3. Install Nexa SDK 🛠️

#### CPU Installation

To install the CPU version of Nexa SDK, run:

```bash
pip install nexaai --prefer-binary --index-url https://nexaai.github.io/nexa-sdk/whl/cpu --extra-index-url https://pypi.org/simple --no-cache-dir
```

#### GPU Installation (Metal - macOS)

For the GPU version supporting Metal (macOS), run:

```bash
CMAKE_ARGS="-DGGML_METAL=ON -DSD_METAL=ON" pip install nexaai --prefer-binary --index-url https://nexaai.github.io/nexa-sdk/whl/metal --extra-index-url https://pypi.org/simple --no-cache-dir
```

For detailed installation instructions of Nexa SDK for **CUDA** and **AMD GPU** support, please refer to the [Installation section](https://github.com/NexaAI/nexa-sdk?tab=readme-ov-file#installation) in the main README.

### 4. Install Dependencies

Ensure you are in the project directory and install the required dependencies using `requirements.txt`:

```zsh
pip install -r requirements.txt
```

**Note:** If you encounter issues with any packages, install them individually:

```zsh
pip install nexa Pillow pytesseract PyMuPDF python-docx
```

With the environment activated and dependencies installed, run the script using:

## Running the Script

```zsh
python main.py
```

The script will:

1. Display the directory tree of your input directory.
2. Inform you that the files have been uploaded and processing will begin.
3. Process each file, generating metadata.
4. Copy and rename the files into the output directory based on the generated metadata.
5. Display the directory tree of your output directory after processing.

**Note:** The actual descriptions, folder names, and filenames will be generated by the AI models based on your files' content.

#### Enter the Input Path

You will be prompted to enter the path of the directory where the files you want to organize are stored. Enter the full path to that directory and press Enter.

```zsh
Enter the path of the directory you want to organize: /path/to/your/input_folder
```

#### Enter the Output Path

Next, you will be prompted to enter the path where you want the organized files to be stored. You can either specify a directory or press Enter to use the default directory (organzied_folder) inside the input directory.

```zsh
Enter the path to store organized files and folders (press Enter to use 'organzied_folder' in the input directory): /path/to/your/output_folder
```

If you press Enter without specifying a path, the script will create a folder named organzied_folder in the input directory to store the organized files.

## Notes

- **SDK Models:**

  - The script uses `NexaVLMInference` and `NexaTextInference` models [usage](https://docs.nexaai.com/sdk/python-interface/gguf).
  - Ensure you have access to these models and they are correctly set up.
  - You may need to download model files or configure paths.

- **Dependencies:**

  - **pytesseract:** Requires Tesseract OCR installed on your system.
    - **macOS:** `brew install tesseract`
    - **Ubuntu/Linux:** `sudo apt-get install tesseract-ocr`
    - **Windows:** Download from [Tesseract OCR Windows Installer](https://github.com/UB-Mannheim/tesseract/wiki)
  - **PyMuPDF (fitz):** Used for reading PDFs.

- **Processing Time:**

  - Processing may take time depending on the number and size of files.
  - The script uses multiprocessing to improve performance.

- **Customizing Prompts:**
  - You can adjust prompts in `data_processing.py` to change how metadata is generated.

## License

This project is dual-licensed under the MIT License and Apache 2.0 License. You may choose which license you prefer to use for this project.

- See the [MIT License](LICENSE-MIT) for more details.
- See the [Apache 2.0 License](LICENSE-Apache-2.0) for more details.
