# Vast.ai Private AI Templates for Qwen 2.5 Models

Access cutting-edge AI models with complete privacy and minimal setup using our custom templates on Vast.ai. Whether you need a powerful language model for personal document processing or an agent workflow that prioritizes uptime over token limits, these templates offer the perfect balance of performance, privacy, and cost-effectiveness.
## About Vast.ai

[Vast.ai](https://cloud.vast.ai/?ref_id=167881) is a cloud marketplace that provides affordable GPU rentals for AI workloads. By leveraging Vast.ai's infrastructure, you can run powerful AI models at a fraction of the cost of traditional cloud providers. With flexible hardware options and transparent pricing, Vast.ai is the perfect solution for individuals and teams looking to maximize performance while keeping costs low.


## Why Choose These Templates?

### 🔒 Complete Privacy
- **No Logging**: Your data stays private with no logging, ensuring the highest level of confidentiality.
- **Self-hosted**: Run models in your own secure instance. No need to worry about third-party data access.

### ⚙️ Simple & Convenient
- **Minimal Setup**: Deploy in just a few steps with pre-configured templates.
- **Optimized for GPUs**: Designed to run on a variety of hardware, including H100, RTX 3090, and RTX 4090, ensuring compatibility for your needs.

### 💰 Cost-Effective
- **Pay Only for Uptime**: No token-based fees, you only pay for the time your instance is running.
- **Flexible Hardware Options**: Choose the setup that fits your budget, from single GPUs to more powerful configurations.
- **Top-Quality Models**: Access optimized, state-of-the-art models without breaking the bank.

---

## Available Templates

### 1. Qwen 2.5-72B Instruct OAI API for 1x H100 GPU
- **Model**: Qwen 2.5-72B Instruct (8-bit quantized, exl2)
- **Hardware**: Single H100, CUDA 12.4
- **VRAM**: 70GB required
- **Cuda**: 12.4

[**Launch Template**](https://cloud.vast.ai/?ref_id=167881&template_id=581b0df498f0062ba1449630e4646e4a)

---

### 2. Qwen 2.5-14B Instruct OAI API for 1x RTX GPU (3090 or 4090)
- **Model**: Qwen 2.5-14B Instruct (8-bit quantized)
- **Hardware**: Single RTX 3090 or 4090
- **VRAM**: 20GB required
- **Cuda**: 12.4

[**Launch Template**](https://cloud.vast.ai/?ref_id=167881&template_id=49097547d4e3219247f395358f5993f6)

---

### 3. Qwen 2.5-72B Instruct OAI API for 2x RTX GPUs
- **Model**: Qwen 2.5-72B Instruct (8-bit quantized)
- **Hardware**: Dual RTX 3090 or 4090
- **VRAM**: 44GB total required
- **Cuda**: 12.4

[**Launch Template**](https://cloud.vast.ai/?ref_id=167881&template_id=02f5a7ee57f6e9aece4c4d6b8b6748c7)

---

## Use Cases

1. **Private Document Processing**: Securely process large batches of documents without worrying about data leaks.
2. **Agent Workflows**: Run long-term agents that don’t rely on token limits—just pay for uptime, no extra costs.
3. **Secure Batch Processing**: Run large batch operations for sensitive data analysis without sacrificing confidentiality.
5. **Research and Development**: Perfect for individuals or small companies looking for efficient AI model execution without compromising on security.

---

## Features

- **No Token Fees**: Pay only for uptime—no additional token costs.
- **OpenAI-Compatible API**: Use standard OpenAI-style completions and chat requests.
- **Full Privacy**: Keep all data confidential with no logging and no third-party access.
- **Optimized for Various GPUs**: Choose between H100, RTX 3090, or 4090 for your model deployment.
- **Fast Setup**: Pre-configured templates with minimal setup required.

---

## How to Use the Templates

### 1. **Select the Template**
   - Choose the hardware/template combo - The larger the model the better the performance.
   - For example, if you want the best experience choose a H100 GPU, Cuda12.4 and use the template below optimised for that hardware.

### 2. **Start the Instance**
   - Launch the instance and wait for the setup to complete.
   - It may take a few minutes for the instance to load and start.

### 3. **Add SSH Key**
   - Add your SSH key to the instance by following the prompts on the Vast.ai dashboard.

### 4. **Connect via SSH**
   - Use the provided connection string to access the instance terminal.

### 5. **Run the LLM Server**
   - Navigate to the root directory and start the model server:
     ```bash
     cd /
     app/entrypoint.sh
     ```
   - Wait for the model files to download and initialize. 

### 6. **API Access**
   - Copy your API key from the instance log and start making requests using the OpenAI-compatible API.

### 7. **Example API Requests**

#### Curl:
```bash
curl http://<instance-ip>:5000/v1/completions \
  -H "x-api-key:<your-api-key>" \
  -H "Content-Type: application/json" \
  -d '{
        "prompt": "What is the capital of France?",
        "parameters": {
            "temperature": 0.7,
            "max_tokens": 256
        }
      }'
```

#### Python:
```python
import requests
import json

url = "http://<instance-ip>:5000/v1/completions"
headers = {
    "Content-Type": "application/json",
    "x-api-key": "<your-api-key>"
}
data = {
    "prompt": "What is the capital of France?",
    "parameters": {
        "temperature": 0.7,
        "max_tokens": 256
    }
}
response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
```

---

## Ready to Get Started?

Sign up on Vast.ai with [this referral link](https://cloud.vast.ai/?ref_id=167881) and access top-tier models with our templates!

---
