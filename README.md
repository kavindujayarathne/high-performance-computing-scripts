# High Performance Computing Scripts

This repository contains a collection of high performance computing scripts I have written in C. These scripts showcase the use of multithreading and GPU acceleration for various computational tasks.

## Scripts Included

<ul>
  <li>Matrix Multiplication with Multithreading</li>
  <li>Password Cracking using Multithreading</li>
  <li>Password Cracking using CUDA</li>
  <li>Box Blur using CUDA</li>
</ul>

## Getting Started

### Using Google Colab

You can run these scripts directly in Google Colab, which provides a convenient environment with necessary libraries pre-installed.

To run the GPU-related tasks on Google Colab, change the runtime type to use a T4 GPU. For other tasks, the CPU runtime type is sufficient.

### Using Visual Studio Code

To run these scripts in Visual Studio Code, follow these steps to set up the environment:

<strong>Open the Script:</strong> Open the script in Visual Studio Code.

<strong>Select a Kernel:</strong> A kernel is a computational engine that executes the code contained in the notebook cells. When you open a notebook in VS Code, you need to select a kernel to run the code.

<ul>
  <li>In the upper right corner of VS Code, click on the option called 'Select Kernel'.</li>

  <li>If you haven't already installed the relevant Jupyter extensions, VS Code will suggest you install them first.</li>
  <br>

![demo-img 1](https://raw.githubusercontent.com/kavindujayarathne/high-performance-computing-scripts/main/demo-img1.png)

  <li>Once the Jupyter extensions are installed, VS Code will usually handle the next steps automatically.</li>

  <li>If you have already installed Python, VS Code will automatically set that environment as the kernel.</li>

  <li>If it is not selected automatically, the 'Select Kernel' option will still be available. Click on it.</li>

  <li>You will see two options: Python Environments and Existing Jupyter Server.</li>
  <br>

![demo-img 2](https://raw.githubusercontent.com/kavindujayarathne/high-performance-computing-scripts/main/demo-img2.png)

  <ul>
    <li>If you have Python installed on your system, choose Python Environments and select the relevant Python environment.</li>
    <li>If you have a Jupyter server on the cloud or elsewhere, choose Existing Jupyter Server and connect to it.</li>
  </ul>
</ul>

<strong>Install 'ipykernel':</strong>

```
pip install ipykernel
```

<ul>
  <li>Ensure the 'ipykernel' package is installed in your environment to act as a Jupyter kernel, enabling you to run cells within your notebook.</li>

  <li>If connecting to an existing Jupyter server, ensure the server has the ipykernel package installed</li>
</ul>

<strong>Set Up the C Environment:</strong> Install the necessary extensions and C compilers to setup the C Environment, as these scripts are written in C.

<strong>Install CUDA Toolkit:</strong> When using VS Code, to run GPU-accelerated tasks, install the CUDA toolkit on your machine.

<strong>Compile and Execute in the Terminal:</strong>

When you use VS Code, It't better to use the integrated terminal rather than running them inside a cell or using magic commands (!).

<mark><strong>Examples</strong></mark>

You should navigate to the correct directory where your scripts are located before running the commands.

<strong>For C scripts:</strong>

```
gcc -pthread -o matrix_multiplication matrix_multiplication.c
./matrix_multiplication input.txt 6
```

<strong>For CUDA scripts:</strong>

```
nvcc -o enc encrypt.cu
./enc
```

<br>

> **Note:**
>
> These scripts were developed and tested on Google Colab. If you are running them on VS Code, you should setup the environment accordingly.
>
> The scripts utilizing GPU acceleration require a compatible NVIDIA GPU and the CUDA toolkit installed on your machine if you are running GPU-related scripts on VS Code. For Google Colab, GPU support is provided.

## Legal and Ethical Considerations

> **Disclaimer:** These scripts are provided for educational purposes only.

## Licensing

This repository is licensed under the MIT License. See the [`LICENSE`](https://github.com/kavindujayarathne/high-performance-computing-scripts/blob/main/LICENSE) file for more details.

Some scripts include third-party code with its own licenses. Please see the [`THIRD_PARTY_LICENSES.md`](./THIRD_PARTY_LICENSES.md) file for details.
