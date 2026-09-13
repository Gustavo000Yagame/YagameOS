<div align="center">

#  YagameOS

<img src="https://img.shields.io/badge/Platform-Raspberry%20Pi%203-c51a4a?style=for-the-badge&logo=raspberry-pi&logoColor=white" />
<img src="https://img.shields.io/badge/Kernel-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Buildroot-LTS-CC5500?style=for-the-badge&logo=buildroot&logoColor=white" />
<img src="https://img.shields.io/badge/Graphics-DRM%2FKMS%20%2F%20SDL2-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" />

*Um sistema operacional embarcado minimalista e focado em alta performance para jogos e retroemulação.*

</div>

---

## ⚡ O que é o YagameOS?

O **YagameOS** foi desenhado do zero para extrair o máximo do hardware limitado do **Raspberry Pi 3 (armhf)**. Em vez de usar distros pesadas cheias de serviços desnecessários, ele roda um **kernel Linux customizado** direto sobre o hardware, inicializando em segundos com uma interface gráfica própria via **DRM/KMS e SDL2**.

<img width="1425" height="900" alt="image" src="https://github.com/user-attachments/assets/1e3753fd-c81e-4f8e-b174-c55574bcc16f" /> 

```text
+-------------------------------------------------------------+
|                     YAGAME OS ARCHITECTURE                  |
+-------------------------------------------------------------+
|  [ Yagame Launcher / Core ] (C++ / SDL2 / OpenGL ES 2.0)    |
+-------------------------------------------------------------+
|  [ Subsystem Layer ]        (DRM/KMS, uinput, Alsa/Audio)   |
+-------------------------------------------------------------+
|  [ Linux Kernel (armhf) ]   (Custom Buildroot Toolchain)    |
+-------------------------------------------------------------+
|  [ Hardware Target ]        (Raspberry Pi 3 Model B/B+)     |
+-------------------------------------------------------------+
```

<img width="461" height="303" alt="image" src="https://github.com/user-attachments/assets/59b06522-3fdc-44d1-be72-22e0b2dd00fc" />

```
🚀 Principais Características
Boot Instantâneo: Sem gerenciadores de boot pesados (como U-Boot) ou initramfs no MVP.

Gráficos Diretos: Sem servidores gráficos pesados (X11/Wayland). A aplicação desenha direto na controladora de vídeo via DRM/KMS.

Userland Otimizado: Compilação nativa em 32-bit (armhf) para garantir compatibilidade máxima com dynarecs de emuladores.

Sistema Resiliente: Estrutura pronta para rootfs em modo somente-leitura para evitar corrupção de dados ao desligar na tomada.

📁 Estrutura do Repositório
Plaintext
YagameOS/
├── buildroot/          # Base do sistema de compilação LTS
├── yagame-external/    # Configurações de board, pacotes e device tree
├── yagame/             # Código-fonte da aplicação e interface (C/C++)
└── scripts/            # Automação de builds e geração de imagem
🛠️ Status do Desenvolvimento
[x] Fase 0: Setup do ambiente WSL2, compilação cruzada e validação de boot serial no hardware.

[ ] Fase 1: Integração do subsistema gráfico SDL2 e primeiro loop de renderização.

[ ] Fase 2: Implementação do gerenciador de entradas (uinput / controles).

```



