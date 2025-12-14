## Format Conversion: safetensors → GGUF

### Terminal: PowerShell

### Create a Virtual Environment

`conda create -n gguf python=3.10 -y
conda activate gguf`

### Successful Activation

`(gguf) C:\Users\xxxxx>`

---

## Download Hugging Face CLI

### Install Hugging Face CLI

`powershell -ExecutionPolicy ByPass -c "irm https://hf.co/cli/install.ps1 | iex"`

### Download Model

``hf download Qwen/Qwen3-1.7B `  --local-dir D:\llama\models\qwen3-1.7b `  --resume``

- `local-dir`: specifies the download directory

- `resume`: supports resumable downloads

---

## Download llama.cpp (Includes `convert_hf_to_gguf.py`)

### Download Repository ZIP

`https://github.com/ggerganov/llama.cpp/archive/refs/heads/master.zip`

### Extract To

`D:\llama\llama_src\`

### Install Dependencies

`pip install transformers sentencepiece accelerate protobuf pip uninstall -y gguf   # Must be uninstalled to avoid conflicts`

---

## Convert to F16 GGUF

### Conversion Script Location

`D:\llama\llama_src\convert_hf_to_gguf.py`

### Run Conversion

``python D:\llama\llama_src\convert_hf_to_gguf.py `   D:\llama\models\qwen3-1.7b `   --outfile D:\llama\models\qwen3-1.7b-f16.gguf``

### Output

`qwen3-1.7b-f16.gguf`

---

## Quantization

### Quantization Tool

`D:\llama\llama.cpp\llama-quantize.exe`

### Run Quantization

``D:\llama\llama.cpp\llama-quantize.exe `   D:\llama\llama_src\qwen3-1.7b-f16.gguf `   D:\llama\llama_src\qwen3-1.7b-q5_k_m.gguf `   q5_k_m``

- The last parameter (`q4_k_m`, `q5_k_m`, `q8_0`) determines the quantization format

### Output

`qwen3-1.7b-q4_k_m.gguf`

---

## Test the Model

``D:\llama\llama.cpp\llama-cli.exe `   -m D:\llama\llama_src\qwen3-1.7b-q4_k_m.gguf `   -p "who are you"``

---

## Notes

### Common Quantization Formats

- `q5_k_m`

- `q4_k_s`

- `q2_k`

- `q8_0`

### Suffix Meaning

- `k`: K-block (better precision)

- `M` (Mixed): mixed quantization, higher precision than `S`

- `S` (Symmetric): symmetric quantization
