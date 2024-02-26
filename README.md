#언어 모델


tokenizer
![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/98a48d8d-7c1a-44f1-9f21-dde3584bd3d3)

대표적인 언어모델 bert, gpt

bert - bidirectional representations from transformers
transformer 의 인코더만을 사용
![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/3cf1fc2e-af6e-4b6d-bc40-c7b59b965050)


gpt -
transformer의 decoder 블럭 사용 


최근 가장 성능 좋은 llama, MOE(mixture of mistral)



llama 

특징
multihead attention - KV cache,sliding attention
positional embedding - rotary positioanl embedding 사용
activation - swiglu
normalization방법 layernorm- RMSnorm

![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/91f7fb96-7ec7-4746-9354-66ca8d3ef96d)



mistral 7b moe
다양한 task를 expert로 세분화해서 수행

특징 
multihead attention - sliding attention,rolling buffer cache/prefill and chunking(kv cache) llama 와 같음

![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/606a7d26-00c1-4029-a1af-86a2cd38f870)

sparse mixture of experts

![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/d82a0783-6ddf-4562-ba08-134f1c1f924b)


multimodal llm 
텍스트 이미지 오디오 모두 사용하는 언어모델

llava text+ image - embedding방식이 stable diffusion과 유사
![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/4d65831c-e04e-403f-b7a4-d1542a329136)


번외 moe+llava

![image](https://github.com/jinuk0211/tokenizer-mini_byte_pair_encoding/assets/150532431/6a0b6d60-e7f9-4fec-8685-5c14bea674da)
