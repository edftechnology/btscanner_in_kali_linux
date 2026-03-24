# Como configurar/instalar/usar o `btscanner` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `btscanner` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to configure/install/use the `btscanner` on `Linux Ubuntu`._

## Descrição [1][2]

### `btscanner`

O btscanner é uma ferramenta de linha de comando utilizada para explorar dispositivos Bluetooth ao redor, identificando e listando serviços disponíveis e informações sobre dispositivos detectados. Ele permite aos usuários escanear o ambiente em busca de dispositivos Bluetooth ativos, exibindo detalhes como endereços MAC, nomes dos dispositivos e serviços oferecidos, facilitando a análise e o monitoramento de redes Bluetooth em um ambiente específico.


## 1. Configurar/Instalar o `btscanner` no `Linux Ubuntu` [1]

Para instalar o `btscanner` no `Linux Ubuntu`, você pode usar o gerenciador de pacotes `snap`. Siga os passos abaixo:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```
   

3. **Instale o `btscanner`**: Agora, você pode instalar o `btscanner` usando o gerenciador de pacotes `apt`. Execute o comando: `sudo apt install btscanner -y`

4. **Verifique a instalação**: Após a instalação, você pode verificar se o `btscanner` foi instalado corretamente executando: `btscanner --version`

Este comando deve mostrar a versão do btscanner instalada, indicando que a instalação foi bem-sucedida.


## 2. Código completo para configurar/instalar

Para instalar o `btscanner` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install btscanner -y
    btscanner --version
    ```

## Referências

[1] OPENAI. ***Instale btscanner no Ubuntu..*** Disponível em: <https://chatgpt.com/c/6170c111-c77c-498f-afad-3ccf5b25fe42> (texto adaptado). ChatGPT. Acessado em: 25/10/2023 13:08.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 14/11/2023 09:33.
