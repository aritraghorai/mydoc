---
{"dg-publish":true,"permalink":"/notes/internal-project/llm-poc/vllm-task/","title":"Setting Up Vllm in Compute engine"}
---

## Setting up Vps for VLLm
### 1.Install NVIDIA Drivers [Reddit Link](https://www.reddit.com/r/linux4noobs/comments/18n34c3/nvidia_drivers_for_debian_12_step_by_step/) 
***Using Debian 12 as operating System***

1. **Add Non-Free Repositories**: Debian's default repositories don't include proprietary drivers, so you'll need to add the non-free repositories. Edit your `/etc/apt/sources.list` file and add `non-free` to the end of each line. For example, a line in your `sources.list` file might look like this:  
    `deb http://deb.debian.org/debian/ bullseye main contrib non-free`
    
2. **Update Package Lists**: After updating your `sources.list`, run the following command to update your package lists:  
    `sudo apt update`
    
3. **Install Kernel Headers**: The NVIDIA drivers require kernel headers to be installed. You can install them with:  
    `sudo apt install linux-headers-$(uname -r)`
    
4. **Install NVIDIA Drivers**: Install the NVIDIA drivers using the following command:  
    `sudo apt install nvidia-driver`
    
5. **Reboot Your System**: Once the installation is complete, reboot your system to load the drivers:  
    `sudo reboot`
    
6. **Verify the Installation**: After rebooting, you can verify that the NVIDIA drivers are in use with the following command:  
    `sudo nvidia-smi`
    
7. **Troubleshooting**: If you encounter any issues, check the logs for any errors related to NVIDIA. Sometimes, issues can arise due to conflicts with the Nouveau driver, in which case you might need to blacklist the Nouveau driver.

### 2. Install Docker 
[Debian | Docker Docs](https://docs.docker.com/engine/install/debian/)

```sh
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
### 3. Install Nvidia Docker Toolkit
[Installing the NVIDIA Container Toolkit — NVIDIA Container Toolkit 1.16.0 documentation](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#configuring-docker)
```sh
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
  && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
    sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
    sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list


sudo apt-get update

sudo apt-get install -y nvidia-container-toolkit

sudo nvidia-ctk runtime configure --runtime=docker

sudo systemctl restart docker
```

### 4. Running Vllm 
#### Docker compose File -`compose.yml`
```yml
version: "3.8"

services:
  vllm-openai:
    image: vllm/vllm-openai:latest
    runtime: nvidia
    deploy:
      resources:
        reservations:
          devices:
            - capabilities: [gpu]
    environment:
      HUGGING_FACE_HUB_TOKEN: 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
      PYTORCH_CUDA_ALLOC_CONF: expandable_segments:True
    volumes:
      - ~/.cache/huggingface:/root/.cache/huggingface
    ports:
      - "8002:8000"
    ipc: host
    command: --model meta-llama/Meta-Llama-3.1-8B-Instruct --gpu-memory-utilization=.9
```

***In Commands We can add different types of vllm arguments***

[Sampling Parameters — vLLM](https://docs.vllm.ai/en/latest/dev/sampling_params.html)

## References

[NVIDIA Drivers for Debian 12 - Step by Step : r/linux4noobs](https://www.reddit.com/r/linux4noobs/comments/18n34c3/nvidia_drivers_for_debian_12_step_by_step/)
[Debian | Docker Docs](https://docs.docker.com/engine/install/debian/)
[CUDA Installation Guide for Linux](https://docs.nvidia.com/cuda/archive/12.4.1/cuda-installation-guide-linux/index.html#debian)
[Installing the NVIDIA Container Toolkit — NVIDIA Container Toolkit 1.16.0 documentation](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#configuring-docker)


