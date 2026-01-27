# Running llama.cpp

## 1. Clone the Repository

`mkdir llm
cd ~/llm
git clone https://github.com/ggerganov/llama.cpp.git`


If cloning fails:

`cd ~/llm-benchmark
wget -c https://github.com/ggerganov/llama.cpp/archive/refs/heads/master.zip -O llama.cpp.zip
unzip llama.cpp.zip
mv llama.cpp-master llama.cpp
rm llama.cpp.zip`



## 2.Build

`cd llama.cpp
cmake -B build
cmake --build build -j`


