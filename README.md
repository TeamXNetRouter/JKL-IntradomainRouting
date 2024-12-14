<h1 align="center">
  <br>
    <img src="pict/logo.png" alt="logo" width="200">
</h1>

# Intra Domain Routing
Welcome to the Intra Domain Routing Repository. This documentation will guide you through understanding and setting up Intra Domain Routing on your system. You will find all the necessary information and tools in this comprehensive guide.

## Table of Contents
1. [Configuration](#configuration)
2. [Prerequisites](#prerequisites)
3. [Steps](#steps)

# Configuration
<h1 align="center">
  <br>
    <img src="pict/configuration.png" alt="configuration" width="1000">
</h1>

# Prerequisites
Before proceeding with the setup, ensure that you have the following prerequisites:

1. **Ubuntu**: If you are using Windows, you can download Ubuntu from:
    [Ubuntu](https://ubuntu.com/desktop/wsl)

2. **Mininet**: Download Mininet from:
    [Mininet](https://mininet.org/)

3. Navigate to the Mininet directory:

    ```bash
    cd mininet
    ```

4. Install all Mininet dependencies by running the following command:

    ```bash
    ./util/install.sh -a
    ```

5. Once the installation is complete, you can proceed with the next steps.

# Steps
Follow the instructions below to get the system up and running:

1. Clone the repository:

    ```bash
    git clone https://github.com/TeamXNetRouter/JKL-IntradomainRouting
    ```

2. Navigate to the project directory:

    ```bash
    cd intradomain-routing
    ```

3. Run the project using the following command:

    ```bash
    sudo python3 ospf-topo.py -c frr-config
    ```

4. To test the setup, you can use the following command in the terminal:

    ```bash
    C1_1 traceroute -I C3_2
    ```

5. Even if the link between R1 and R3 is down, you can still perform a traceroute:

    ```bash
    link R1 R3 down
    C1_1 traceroute -I C3_2
    ```
